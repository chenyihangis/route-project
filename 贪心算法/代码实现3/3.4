import datetime
import math
import matplotlib.pyplot as plt

from greedyAlg3Data import coordinates1, coordinates2, coordinates1goods, coordinates2goods, truck_coordinates

start_time = datetime.datetime.now()


class Site:
    def __init__(self, x, y, ifo, goods):
        self.x = x
        self.y = y
        self.store = 0
        self.need = 0
        self.map = []
        self.description = ifo
        if ifo == "req":
            self.need = goods
        elif ifo == "sup":
            self.store = goods

    def __str__(self):
        return '[{},{}]+{}+{}+{}'.format(self.x, self.y, self.description, self.store, self.need)


sites = []
for i in range(len(coordinates1)):
    sites.append(Site(coordinates1[i][0], coordinates1[i][1], "req", coordinates1goods[i]))
for i in range(len(coordinates2)):
    sites.append(Site(coordinates2[i][0], coordinates2[i][1], "sup", coordinates2goods[i]))


def length(x1, y1, x2, y2):
    return math.sqrt((int(x1) - int(x2)) ** 2 + (int(y1) - int(y2)) ** 2)  # 用于计算路径表


req_count = 0
for i in coordinates1goods:
    req_count += i

sup_count = 0
for i in coordinates2goods:
    sup_count += i


class UAV:
    def __init__(self, x, y, volume, num):
        self.x = x
        self.y = y
        self.volume = volume
        self.covered_dis = 0
        self.draw_path = []
        self.capacity = 0
        self.at = Site(0, 0, 0, 0)
        self.number = num

    def __str__(self):
        return '坐标: [{},{}]当前运载的货量: {} 总共走了{}距离 '.format(self.x, self.y, self.capacity, self.covered_dis)

    def draw_picture(self):
        color = ['b', 'g', 'r', 'c']
        for k in range(len(coordinates1)):
            plt.plot(coordinates1[k][0], coordinates1[k][1], 'r', marker='o')  # 红色 需求点坐标为o
        for k in range(len(coordinates2)):
            plt.plot(coordinates2[k][0], coordinates2[k][1], 'b', marker='>')  # 蓝色 供应点坐标为>
        for k in range(len(self.draw_path) - 1):
            plt.plot((self.draw_path[k][0], self.draw_path[k + 1][0]),
                     (self.draw_path[k][1], self.draw_path[k + 1][1]),
                     color[self.number % 4])
        plt.title('car: ' + str(self.number), fontsize=30)
        plt.show()
        plt.close()

    def next_site(self):
        def updadte(goto, uav):
            global req_count
            global sup_count
            if goto == "closest":
                for poi in uav.at.map:
                    if poi[1].need + poi[1].store != 0:
                        if poi[1].description == "req":
                            uav.covered_dis += length(uav.x, uav.y, poi[1].x, poi[1].y)
                            uav.draw_path.append([uav.x, uav.y])
                            uav.at = poi[1]
                            uav.x = poi[1].x
                            uav.y = poi[1].y
                            if poi[1].need >= uav.capacity:
                                poi[1].need -= uav.capacity
                                req_count -= uav.capacity
                                uav.capacity = 0
                            else:
                                uav.capacity -= poi[1].need
                                req_count -= poi[1].need
                                poi[1].need = 0
                            break
                        elif poi[1].description == "sup":
                            uav.covered_dis += length(uav.x, uav.y, poi[1].x, poi[1].y)
                            uav.draw_path.append([uav.x, uav.y])
                            uav.at = poi[1]
                            uav.x = poi[1].x
                            uav.y = poi[1].y
                            if poi[1].store >= uav.volume - uav.capacity:
                                poi[1].store -= (uav.volume - uav.capacity)
                                sup_count -= (uav.volume - uav.capacity)
                                uav.capacity = uav.volume
                            else:
                                uav.capacity += poi[1].store
                                sup_count -= poi[1].store
                                poi[1].store = 0
                            break
            elif goto == "sup":
                for poi in uav.at.map:
                    if poi[1].description == "sup" and poi[1].store != 0:
                        uav.covered_dis += length(uav.x, uav.y, poi[1].x, poi[1].y)
                        uav.draw_path.append([uav.x, uav.y])
                        uav.at = poi[1]
                        uav.x = poi[1].x
                        uav.y = poi[1].y
                        if poi[1].store >= (uav.volume - uav.capacity):
                            poi[1].store -= (uav.volume - uav.capacity)
                            sup_count -= (uav.volume - uav.capacity)
                            uav.capacity = uav.volume
                        else:
                            uav.capacity += poi[1].store
                            sup_count -= poi[1].store
                            poi[1].store = 0
                        break
            elif goto == "req":
                for poi in uav.at.map:
                    if poi[1].description == "req" and poi[1].need != 0:
                        uav.covered_dis += length(uav.x, uav.y, poi[1].x, poi[1].y)
                        uav.draw_path.append([uav.x, uav.y])
                        uav.at = poi[1]
                        uav.x = poi[1].x
                        uav.y = poi[1].y
                        if poi[1].need >= uav.capacity:
                            poi[1].need -= uav.capacity
                            req_count -= uav.capacity
                            uav.capacity = 0
                        else:
                            uav.capacity -= poi[1].need
                            req_count -= poi[1].need
                            poi[1].need = 0
                        break

        if self.at.description == "sup":
            if self.volume == self.capacity:
                updadte("req", self)
            else:
                updadte("closest", self)
        elif self.at.description == "req":
            if self.capacity == 0:
                updadte("sup", self)
            else:
                updadte("closest", self)


for i in sites:
    for si in sites:
        if i is si:
            continue
        i.map.append([length(i.x, i.y, si.x, si.y), si])
    i.map = sorted(i.map, key=lambda x: x[0])
UAVs = []
for i in range(len(truck_coordinates)):
    UAVs.append(UAV(truck_coordinates[i][0], truck_coordinates[i][1], truck_coordinates[i][2], i))
for i in UAVs:
    li = []
    for si in sites:
        if si.description == "sup":
            li.append([length(i.x, i.y, si.x, si.y), si])
    i.at = min(li, key=lambda x: x[0])[1]
    i.covered_dis += length(i.x, i.y, i.at.x, i.at.y)
    i.draw_path.append([i.x, i.y])
    i.x = i.at.x
    i.y = i.at.y
    if i.at.store >= i.volume:
        i.at.store -= i.volume
        i.capacity = i.volume
        sup_count -= i.volume
    else:
        i.capacity += i.at.store
        sup_count -= i.at.store
        i.at.store = 0
    print(i)
while True:
    if sup_count == 0:
        break
    if req_count == 0:
        break
    for i in UAVs:
        i.next_site()

end_time = datetime.datetime.now()
print()
print('算法时间:', end_time - start_time)
time_list = []
for i in UAVs:
    time_list.append(i.covered_dis)
    for j in range(len(truck_coordinates)):
        plt.plot(truck_coordinates[j][0], truck_coordinates[j][1], 'black', marker='1')  # 黑色 汽车初始位置
    i.draw_picture()
print(max(time_list))
