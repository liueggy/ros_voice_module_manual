# 命令词预处理

<table>
  <tr>
    <th><p>语义标签</p></th>
    <th><p>命令词</p></th>
    <th><p>功能类型</p></th>
    <th><p>播报语句</p></th>
    <th><p>播报模式</p></th>
    <th><p>发送协议</p></th>
    <th><p>接收协议</p></th>
  </tr>
  <tr>
    <td><p>1</p></td>
    <td><p>欢迎语</p></td>
    <td><p>欢迎语</p></td>
    <td><p>欢迎使用小亚</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 01 00 FB</p></td>
    <td><p>AA 55 01 00 FB</p></td>
  </tr>
  <tr>
    <td><p>2</p></td>
    <td><p>休息语</p></td>
    <td><p>休息语</p></td>
    <td><p>我去休息啦</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 02 6F FB</p></td>
    <td><p>AA 55 02 00 FB</p></td>
  </tr>
  <tr>
    <td><p>3</p></td>
    <td><p>你好小亚</p></td>
    <td><p>唤醒词</p></td>
    <td><p>我在</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 03 00 FB</p></td>
    <td><p>AA 55 03 00 FB</p></td>
  </tr>
  <tr>
    <td><p>4</p></td>
    <td><p>增大音量</p></td>
    <td><p>增大音量</p></td>
    <td><p>增大音量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 04 00 FB</p></td>
    <td><p>AA 55 04 00 FB</p></td>
  </tr>
  <tr>
    <td><p>5</p></td>
    <td><p>减小音量</p></td>
    <td><p>减小音量</p></td>
    <td><p>减小音量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 05 00 FB</p></td>
    <td><p>AA 55 05 00 FB</p></td>
  </tr>
  <tr>
    <td><p>6</p></td>
    <td><p>最大音量</p></td>
    <td><p>最大音量</p></td>
    <td><p>最大音量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 06 00 FB</p></td>
    <td><p>AA 55 06 00 FB</p></td>
  </tr>
  <tr>
    <td><p>7</p></td>
    <td><p>中等音量</p></td>
    <td><p>中等音量</p></td>
    <td><p>中等音量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 07 00 FB</p></td>
    <td><p>AA 55 07 00 FB</p></td>
  </tr>
  <tr>
    <td><p>8</p></td>
    <td><p>最小音量</p></td>
    <td><p>最小音量</p></td>
    <td><p>最小音量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 08 00 FB</p></td>
    <td><p>AA 55 08 00 FB</p></td>
  </tr>
  <tr>
    <td><p>9</p></td>
    <td><p>开启播报</p></td>
    <td><p>开播报</p></td>
    <td><p>开启播报</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 09 00 FB</p></td>
    <td><p>AA 55 09 00 FB</p></td>
  </tr>
  <tr>
    <td><p>10</p></td>
    <td><p>关闭播报</p></td>
    <td><p>关播报</p></td>
    <td><p>关闭播报</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 0A 00 FB</p></td>
    <td><p>AA 55 0A 00 FB</p></td>
  </tr>
  <tr>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
  </tr>
  <tr>
    <td><p>11</p></td>
    <td><p>小车停车</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已停止</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 01 FB</p></td>
    <td><p>AA 55 00 01 FB</p></td>
  </tr>
  <tr>
    <td><p>12</p></td>
    <td><p>停车</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已停止</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 02 FB</p></td>
    <td><p>AA 55 00 02 FB</p></td>
  </tr>
  <tr>
    <td><p>13</p></td>
    <td><p>小车休眠</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已休眠</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 03 FB</p></td>
    <td><p>AA 55 00 03 FB</p></td>
  </tr>
  <tr>
    <td><p>14</p></td>
    <td><p>小车前进</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在前进</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 04 FB</p></td>
    <td><p>AA 55 00 04 FB</p></td>
  </tr>
  <tr>
    <td><p>15</p></td>
    <td><p>小车后退</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在后退</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 05 FB</p></td>
    <td><p>AA 55 00 05 FB</p></td>
  </tr>
  <tr>
    <td><p>16</p></td>
    <td><p>小车左转</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在向左转</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 06 FB</p></td>
    <td><p>AA 55 00 06 FB</p></td>
  </tr>
  <tr>
    <td><p>17</p></td>
    <td><p>小车右转</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在向右转</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 07 FB</p></td>
    <td><p>AA 55 00 07 FB</p></td>
  </tr>
  <tr>
    <td><p>18</p></td>
    <td><p>小车左旋</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在向左旋转</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 08 FB</p></td>
    <td><p>AA 55 00 08 FB</p></td>
  </tr>
  <tr>
    <td><p>19</p></td>
    <td><p>小车右旋</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在向右旋转</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 09 FB</p></td>
    <td><p>AA 55 00 09 FB</p></td>
  </tr>
  <tr>
    <td><p>20</p></td>
    <td><p>关灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已关灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0A FB</p></td>
    <td><p>AA 55 00 0A FB</p></td>
  </tr>
  <tr>
    <td><p>21</p></td>
    <td><p>亮红灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已亮红灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0B FB</p></td>
    <td><p>AA 55 00 0B FB</p></td>
  </tr>
  <tr>
    <td><p>22</p></td>
    <td><p>亮绿灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已亮绿灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0C FB</p></td>
    <td><p>AA 55 00 0C FB</p></td>
  </tr>
  <tr>
    <td><p>23</p></td>
    <td><p>亮蓝灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已亮蓝灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0D FB</p></td>
    <td><p>AA 55 00 0D FB</p></td>
  </tr>
  <tr>
    <td><p>24</p></td>
    <td><p>亮黄灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已亮黄灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0E FB</p></td>
    <td><p>AA 55 00 0E FB</p></td>
  </tr>
  <tr>
    <td><p>25</p></td>
    <td><p>打开流水灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已打开流水灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 0F FB</p></td>
    <td><p>AA 55 00 0F FB</p></td>
  </tr>
  <tr>
    <td><p>26</p></td>
    <td><p>打开渐变灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已打开渐变灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 10 FB</p></td>
    <td><p>AA 55 00 10 FB</p></td>
  </tr>
  <tr>
    <td><p>27</p></td>
    <td><p>打开呼吸灯</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已打开呼吸灯</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 11 FB</p></td>
    <td><p>AA 55 00 11 FB</p></td>
  </tr>
  <tr>
    <td><p>28</p></td>
    <td><p>显示电量</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已显示电量</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 12 FB</p></td>
    <td><p>AA 55 00 12 FB</p></td>
  </tr>
  <tr>
    <td><p>29</p></td>
    <td><p>导航去一号位</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在去一号位</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 13 FB</p></td>
    <td><p>AA 55 00 13 FB</p></td>
  </tr>
  <tr>
    <td><p>30</p></td>
    <td><p>导航去二号位</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在去二号位</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 14 FB</p></td>
    <td><p>AA 55 00 14 FB</p></td>
  </tr>
  <tr>
    <td><p>31</p></td>
    <td><p>导航去三号位</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在去三号位</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 15 FB</p></td>
    <td><p>AA 55 00 15 FB</p></td>
  </tr>
  <tr>
    <td><p>32</p></td>
    <td><p>导航去四号位</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在去四号位</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 20 FB</p></td>
    <td><p>AA 55 00 20 FB</p></td>
  </tr>
  <tr>
    <td><p>33</p></td>
    <td><p>回到原点</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，正在回到原点</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 21 FB</p></td>
    <td><p>AA 55 00 21 FB</p></td>
  </tr>
  <tr>
    <td><p>34</p></td>
    <td><p>关闭巡线</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已关闭巡线功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 16 FB</p></td>
    <td><p>AA 55 00 16 FB</p></td>
  </tr>
  <tr>
    <td><p>35</p></td>
    <td><p>巡红线</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启巡红线功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 17 FB</p></td>
    <td><p>AA 55 00 17 FB</p></td>
  </tr>
  <tr>
    <td><p>36</p></td>
    <td><p>巡绿线</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启巡绿线功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 18 FB</p></td>
    <td><p>AA 55 00 18 FB</p></td>
  </tr>
  <tr>
    <td><p>37</p></td>
    <td><p>巡蓝线</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启巡蓝线功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 19 FB</p></td>
    <td><p>AA 55 00 19 FB</p></td>
  </tr>
  <tr>
    <td><p>38</p></td>
    <td><p>巡黄线</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启巡黄线功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 1A FB</p></td>
    <td><p>AA 55 00 1A FB</p></td>
  </tr>
  <tr>
    <td><p>39</p></td>
    <td><p>开启跟随</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启跟随功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 1B FB</p></td>
    <td><p>AA 55 00 1B FB</p></td>
  </tr>
  <tr>
    <td><p>40</p></td>
    <td><p>关闭跟随</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已关闭跟随功能</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 1C FB</p></td>
    <td><p>AA 55 00 1C FB</p></td>
  </tr>
  <tr>
    <td><p>41</p></td>
    <td><p>报警</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已开启报警</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 26 FB</p></td>
    <td><p>AA 55 00 26 FB</p></td>
  </tr>
  <tr>
    <td><p>42</p></td>
    <td><p>向上</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制向上</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 27 FB</p></td>
    <td><p>AA 55 00 27 FB</p></td>
  </tr>
  <tr>
    <td><p>43</p></td>
    <td><p>向下</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制向下</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 28 FB</p></td>
    <td><p>AA 55 00 28 FB</p></td>
  </tr>
  <tr>
    <td><p>44</p></td>
    <td><p>向左</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制向左</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 29 FB</p></td>
    <td><p>AA 55 00 29 FB</p></td>
  </tr>
  <tr>
    <td><p>45</p></td>
    <td><p>向右</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制向右</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2A FB</p></td>
    <td><p>AA 55 00 2A FB</p></td>
  </tr>
  <tr>
    <td><p>46</p></td>
    <td><p>夹紧</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制夹紧</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2B FB</p></td>
    <td><p>AA 55 00 2B FB</p></td>
  </tr>
  <tr>
    <td><p>47</p></td>
    <td><p>松开</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已控制松开</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2C FB</p></td>
    <td><p>AA 55 00 2C FB</p></td>
  </tr>
  <tr>
    <td><p>48</p></td>
    <td><p>鼓掌</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2D FB</p></td>
    <td><p>AA 55 00 2D FB</p></td>
  </tr>
  <tr>
    <td><p>49</p></td>
    <td><p>点头</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2E FB</p></td>
    <td><p>AA 55 00 2E FB</p></td>
  </tr>
  <tr>
    <td><p>50</p></td>
    <td><p>祈祷</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 2F FB</p></td>
    <td><p>AA 55 00 2F FB</p></td>
  </tr>
  <tr>
    <td><p>51</p></td>
    <td><p>跪下</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 30 FB</p></td>
    <td><p>AA 55 00 30 FB</p></td>
  </tr>
  <tr>
    <td><p>52</p></td>
    <td><p>初始位置</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 31 FB</p></td>
    <td><p>AA 55 00 31 FB</p></td>
  </tr>
  <tr>
    <td><p>53</p></td>
    <td><p>惊吓</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 32 FB</p></td>
    <td><p>AA 55 00 32 FB</p></td>
  </tr>
  <tr>
    <td><p>54</p></td>
    <td><p>叠罗汉</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始叠罗汉</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 33 FB</p></td>
    <td><p>AA 55 00 33 FB</p></td>
  </tr>
  <tr>
    <td><p>55</p></td>
    <td><p>跳舞</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始跳舞</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 34 FB</p></td>
    <td><p>AA 55 00 34 FB</p></td>
  </tr>
  <tr>
    <td><p>56</p></td>
    <td><p>夹方块</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始夹方块</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 35 FB</p></td>
    <td><p>AA 55 00 35 FB</p></td>
  </tr>
  <tr>
    <td><p>57</p></td>
    <td><p>搬运</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始搬运</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 36 FB</p></td>
    <td><p>AA 55 00 36 FB</p></td>
  </tr>
  <tr>
    <td><p>58</p></td>
    <td><p>输入完成</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，请输入下一组动作</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 37 FB</p></td>
    <td><p>AA 55 00 37 FB</p></td>
  </tr>
  <tr>
    <td><p>59</p></td>
    <td><p>输入结束</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，已结束</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 38 FB</p></td>
    <td><p>AA 55 00 38 FB</p></td>
  </tr>
  <tr>
    <td><p>60</p></td>
    <td><p>运动动作</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始运行动作</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 39 FB</p></td>
    <td><p>AA 55 00 39 FB</p></td>
  </tr>
  <tr>
    <td><p>61</p></td>
    <td><p>清除动作</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，动作已清除</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 3A FB</p></td>
    <td><p>AA 55 00 3A FB</p></td>
  </tr>
  <tr>
    <td><p>62</p></td>
    <td><p>这是什么颜色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 3C FB</p></td>
    <td><p>AA 55 00 3C FB</p></td>
  </tr>
  <tr>
    <td><p>63</p></td>
    <td><p>开始颜色分拣</p></td>
    <td><p>命令词</p></td>
    <td><p>开始颜色分拣</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 3D FB</p></td>
    <td><p>AA 55 00 3D FB</p></td>
  </tr>
  <tr>
    <td><p>64</p></td>
    <td><p>开始颜色抓取</p></td>
    <td><p>命令词</p></td>
    <td><p>开始颜色抓取</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 46 FB</p></td>
    <td><p>AA 55 00 46 FB</p></td>
  </tr>
  <tr>
    <td><p>65</p></td>
    <td><p>开始追踪人脸</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始追踪人脸</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 47 FB</p></td>
    <td><p>AA 55 00 47 FB</p></td>
  </tr>
  <tr>
    <td><p>66</p></td>
    <td><p>开始追踪黄色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始追踪黄色</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 48 FB</p></td>
    <td><p>AA 55 00 48 FB</p></td>
  </tr>
  <tr>
    <td><p>67</p></td>
    <td><p>开始追踪红色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始追踪红色</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 49 FB</p></td>
    <td><p>AA 55 00 49 FB</p></td>
  </tr>
  <tr>
    <td><p>68</p></td>
    <td><p>开始追踪绿色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始追踪绿色</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4A FB</p></td>
    <td><p>AA 55 00 4A FB</p></td>
  </tr>
  <tr>
    <td><p>69</p></td>
    <td><p>开始追踪蓝色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始追踪蓝色</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4B FB</p></td>
    <td><p>AA 55 00 4B FB</p></td>
  </tr>
  <tr>
    <td><p>70</p></td>
    <td><p>取消追踪</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，取消追踪</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4C FB</p></td>
    <td><p>AA 55 00 4C FB</p></td>
  </tr>
  <tr>
    <td><p>71</p></td>
    <td><p>夹取黄色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始夹取</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4D FB</p></td>
    <td><p>AA 55 00 4D FB</p></td>
  </tr>
  <tr>
    <td><p>72</p></td>
    <td><p>夹取红色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始夹取</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4E FB</p></td>
    <td><p>AA 55 00 4E FB</p></td>
  </tr>
  <tr>
    <td><p>73</p></td>
    <td><p>夹取绿色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始夹取</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 4F FB</p></td>
    <td><p>AA 55 00 4F FB</p></td>
  </tr>
  <tr>
    <td><p>74</p></td>
    <td><p>夹取蓝色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的，开始夹取</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 50 FB</p></td>
    <td><p>AA 55 00 50 FB</p></td>
  </tr>
  <tr>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
  </tr>
  <tr>
    <td><p>75</p></td>
    <td><p>推倒</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 52 FB</p></td>
    <td><p>AA 55 00 52 FB</p></td>
  </tr>
  <tr>
    <td><p>76</p></td>
    <td><p>开始分拣</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 5C FB</p></td>
    <td><p>AA 55 00 5C FB</p></td>
  </tr>
  <tr>
    <td><p>77</p></td>
    <td><p>红色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 57 FB</p></td>
    <td><p>AA 55 00 57 FB</p></td>
  </tr>
  <tr>
    <td><p>78</p></td>
    <td><p>绿色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 58 FB</p></td>
    <td><p>AA 55 00 58 FB</p></td>
  </tr>
  <tr>
    <td><p>79</p></td>
    <td><p>蓝色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 59 FB</p></td>
    <td><p>AA 55 00 59 FB</p></td>
  </tr>
  <tr>
    <td><p>80</p></td>
    <td><p>黄色</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 5A FB</p></td>
    <td><p>AA 55 00 5A FB</p></td>
  </tr>
  <tr>
    <td><p>81</p></td>
    <td><p>不要</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 5B FB</p></td>
    <td><p>AA 55 00 5B FB</p></td>
  </tr>
  <tr>
    <td><p>82</p></td>
    <td><p>这是什么垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>好的</p></td>
    <td><p>主</p></td>
    <td><p>AA 55 00 5E FB</p></td>
    <td><p>AA 55 00 5E FB</p></td>
  </tr>
  <tr>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
  </tr>
  <tr>
    <td><p>83</p></td>
    <td><p>这是红色</p></td>
    <td><p>命令词</p></td>
    <td><p>这是红色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 3D FB</p></td>
    <td><p>AA 55 FF 3D FB</p></td>
  </tr>
  <tr>
    <td><p>84</p></td>
    <td><p>这是蓝色</p></td>
    <td><p>命令词</p></td>
    <td><p>这是蓝色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 3E FB</p></td>
    <td><p>AA 55 FF 3E FB</p></td>
  </tr>
  <tr>
    <td><p>85</p></td>
    <td><p>这是绿色</p></td>
    <td><p>命令词</p></td>
    <td><p>这是绿色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 3F FB</p></td>
    <td><p>AA 55 FF 3F FB</p></td>
  </tr>
  <tr>
    <td><p>86</p></td>
    <td><p>这是黄色</p></td>
    <td><p>命令词</p></td>
    <td><p>这是黄色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 40 FB</p></td>
    <td><p>AA 55 FF 40 FB</p></td>
  </tr>
  <tr>
    <td><p>87</p></td>
    <td><p>识别到黄色</p></td>
    <td><p>命令词</p></td>
    <td><p>识别到黄色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 42 FB</p></td>
    <td><p>AA 55 FF 42 FB</p></td>
  </tr>
  <tr>
    <td><p>88</p></td>
    <td><p>识别到绿色</p></td>
    <td><p>命令词</p></td>
    <td><p>识别到绿色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 43 FB</p></td>
    <td><p>AA 55 FF 43 FB</p></td>
  </tr>
  <tr>
    <td><p>89</p></td>
    <td><p>识别到蓝色</p></td>
    <td><p>命令词</p></td>
    <td><p>识别到蓝色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 44 FB</p></td>
    <td><p>AA 55 FF 44 FB</p></td>
  </tr>
  <tr>
    <td><p>90</p></td>
    <td><p>识别到红色</p></td>
    <td><p>命令词</p></td>
    <td><p>识别到红色</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 49 FB</p></td>
    <td><p>AA 55 FF 49 FB</p></td>
  </tr>
  <tr>
    <td><p>91</p></td>
    <td><p>初始化完成</p></td>
    <td><p>命令词</p></td>
    <td><p>初始化完成</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 58 FB</p></td>
    <td><p>AA 55 FF 58 FB</p></td>
  </tr>
  <tr>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
    <td><p></p></td>
  </tr>
  <tr>
    <td><p>92</p></td>
    <td><p>这是易拉罐,属于可回收垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是易拉罐,属于可回收垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 5E FB</p></td>
    <td><p>AA 55 FF 5E FB</p></td>
  </tr>
  <tr>
    <td><p>93</p></td>
    <td><p>这是旧书包,属于可回收垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是旧书包,属于可回收垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 5F FB</p></td>
    <td><p>AA 55 FF 5F FB</p></td>
  </tr>
  <tr>
    <td><p>94</p></td>
    <td><p>这是报纸,属于可回收垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是报纸,属于可回收垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 60 FB</p></td>
    <td><p>AA 55 FF 60 FB</p></td>
  </tr>
  <tr>
    <td><p>95</p></td>
    <td><p>这是书本,属于可回收垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是书本,属于可回收垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 61 FB</p></td>
    <td><p>AA 55 FF 61 FB</p></td>
  </tr>
  <tr>
    <td><p>96</p></td>
    <td><p>这是注射器,属于有毒垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是注射器,属于有毒垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 62 FB</p></td>
    <td><p>AA 55 FF 62 FB</p></td>
  </tr>
  <tr>
    <td><p>97</p></td>
    <td><p>这是废旧电池,属于有毒垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是废旧电池,属于有毒垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 63 FB</p></td>
    <td><p>AA 55 FF 63 FB</p></td>
  </tr>
  <tr>
    <td><p>98</p></td>
    <td><p>这是过期化妆品,属于有毒垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是过期化妆品,属于有毒垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 64 FB</p></td>
    <td><p>AA 55 FF 64 FB</p></td>
  </tr>
  <tr>
    <td><p>99</p></td>
    <td><p>这是过期药品,属于有毒垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是过期药品,属于有毒垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 65 FB</p></td>
    <td><p>AA 55 FF 65 FB</p></td>
  </tr>
  <tr>
    <td><p>100</p></td>
    <td><p>这是鱼骨,属于湿垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是鱼骨,属于湿垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 66 FB</p></td>
    <td><p>AA 55 FF 66 FB</p></td>
  </tr>
  <tr>
    <td><p>101</p></td>
    <td><p>这是西瓜皮,属于湿垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是西瓜皮,属于湿垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 67 FB</p></td>
    <td><p>AA 55 FF 67 FB</p></td>
  </tr>
  <tr>
    <td><p>102</p></td>
    <td><p>这是苹果核,属于湿垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是苹果核,属于湿垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 68 FB</p></td>
    <td><p>AA 55 FF 68 FB</p></td>
  </tr>
  <tr>
    <td><p>103</p></td>
    <td><p>这是鸡蛋壳,属于湿垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是鸡蛋壳,属于湿垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 69 FB</p></td>
    <td><p>AA 55 FF 69 FB</p></td>
  </tr>
  <tr>
    <td><p>104</p></td>
    <td><p>这是一次性筷子,属于干垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是一次性筷子,属于干垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 6A FB</p></td>
    <td><p>AA 55 FF 6A FB</p></td>
  </tr>
  <tr>
    <td><p>105</p></td>
    <td><p>这是烟蒂,属于干垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是烟蒂,属于干垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 6B FB</p></td>
    <td><p>AA 55 FF 6B FB</p></td>
  </tr>
  <tr>
    <td><p>106</p></td>
    <td><p>这是桃核,属于干垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是桃核,属于干垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 6C FB</p></td>
    <td><p>AA 55 FF 6C FB</p></td>
  </tr>
  <tr>
    <td><p>107</p></td>
    <td><p>这是卫生纸,属于干垃圾</p></td>
    <td><p>命令词</p></td>
    <td><p>这是卫生纸,属于干垃圾</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 5D FB</p></td>
    <td><p>AA 55 FF 5D FB</p></td>
  </tr>
  <tr>
    <td><p>108</p></td>
    <td><p>放置完成</p></td>
    <td><p>命令词</p></td>
    <td><p>放置完成</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 41 FB</p></td>
    <td><p>AA 55 FF 41 FB</p></td>
  </tr>
  <tr>
    <td><p>109</p></td>
    <td><p>我刚夹取了</p></td>
    <td><p>命令词</p></td>
    <td><p>我刚夹取了</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 22 FB</p></td>
    <td><p>AA 55 FF 22 FB</p></td>
  </tr>
  <tr>
    <td><p>110</p></td>
    <td><p>我可以开始动作输入</p></td>
    <td><p>命令词</p></td>
    <td><p>我可以开始动作输入</p></td>
    <td><p>被</p></td>
    <td><p>AA 55 FF 1D FB</p></td>
    <td><p>AA 55 FF 1D FB</p></td>
  </tr>
  <tr>
    <td><p>111</p></td>
    <td><p>原地转圈</p></td>
    <td><p>命令词</p></td>
    <td><p>开始原地转圈</p></td>
    <td><p>主</p></td>
    <td><p>7B 00 00 00 00 00 00 01 F4 8E 7D</p></td>
    <td><p>7B 00 00 00 00 00 00 01 F4 8E 7D</p></td>
  </tr>
</table>

<table>
  <tr>
    <th rowspan="10"><p>协议固定
不可更改</p></th>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
  <tr>
  </tr>
</table>

# 填写说明

<table>
  <tr>
    <th rowspan="12"><p></p></th>
    <th><p></p></th>
  </tr>
  <tr>
    <td><p>中文命令词</p></td>
  </tr>
  <tr>
    <td><p>1、一般为4-6个字，4个字最佳，过短容误识高，过长不便用户呼叫和记忆；</p></td>
  </tr>
  <tr>
    <td><p>2、命令词中相邻汉字的声韵母区分度越大越好；</p></td>
  </tr>
  <tr>
    <td><p>3、符合用户的语言习惯，是常用的说法，内容具体直接；</p></td>
  </tr>
  <tr>
    <td><p>4、应避免使用日常用语，如：“吃饭啦”;</p></td>
  </tr>
  <tr>
    <td><p>5、生僻字和零声母字应尽量避免，如“语音识别”中“语音”两个字均为零声母字;</p></td>
  </tr>
  <tr>
    <td><p>6、命令词中的字最好不要有语气词，如“啊”、“呢”等;</p></td>
  </tr>
  <tr>
    <td><p>7、应避免使用叠词，如：“你好你好”;</p></td>
  </tr>
  <tr>
    <td><p>8、中文命令词中只能由纯汉字组成,不允许有空格,逗号等其他字符;</p></td>
  </tr>
  <tr>
    <td><p>9、命令词中的数字需要以汉字表示，如“调高一度”、“二十六度”</p></td>
  </tr>
  <tr>
    <td><p>10、若您还未确定命令词，建议您从平台的“命令词推荐”中选择。
命令词推荐【https://document.chipintelli.com/%E8%BD%AF%E4%BB%B6%E5%BC%80%E5%8F%91/%E5%91%BD%E4%BB%A4%E8%AF%8D%E6%8E%A8%E8%8D%90/】
唤醒词推荐【https://document.chipintelli.com/%E8%BD%AF%E4%BB%B6%E5%BC%80%E5%8F%91/%E5%94%A4%E9%86%92%E8%AF%8D%E6%8E%A8%E8%8D%90/】</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>语义标签</p></th>
  </tr>
  <tr>
    <td><p>1、语义标签用于标记同一语义的命令词</p></td>
  </tr>
  <tr>
    <td><p>2、相同语义的命令词，语义标签一样，如：“打开空调”、“开启空调”、“开空调”的语义标签必须相同</p></td>
  </tr>
  <tr>
    <td><p>3、语义标签为正整数，取值范围为：1~65535</p></td>
  </tr>
  <tr>
    <td><p>4、相同语义命令词的播报语句内容可以一样，也可以不一样。播报语句内容一样时，平台会自动根据播报音内容进行去重；播报语句不一样时，当识别到该语义的任何一个命令词时，系统进行随机播报。</p></td>
  </tr>
  <tr>
    <td><p>5、相同语义命令词的发送协议和接收协议必须一样。如果存在不一样，平台自动进行提示。</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>命令词类型</p></th>
  </tr>
  <tr>
    <td><p>1、命令词有三种类型：唤醒词、命令词、负性词。唤醒词用于唤醒语音系统，如“智能管家”；命令词即语音指令词，如“打开空调”；负性词用于降低非命令词语音的误识别，如，当在噪声条件下说“打开电视”时，有概率触发“打开空调”的指令，但“打开电视”非命令词指令，此时，可将“打开电视”标记为负性词加入，以降低“打开空调”的误识别。</p></td>
  </tr>
  <tr>
    <td><p>2、播报语句有两种类型：播报语、欢迎语、休息语。播报语仅用于播报，当语音模组接收到指定播报内容的串口协议时进行播报；欢迎语用于上电播报，提示系统上电成功；休息语是指语音系统从已唤醒的转台切换到非唤醒的状态进行提示的播报。</p></td>
  </tr>
  <tr>
    <td><p>3、当播报语的类型标记为“欢迎语”时，其对应的命令词可用“欢迎语”进行占位；当播报语的类型标记为“休息语”时，其对应的命令词可用“休息语”进行占位。</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>中文播报语句</p></th>
  </tr>
  <tr>
    <td><p>1、播报语句为播报的文本内容，一般为10字以内，语句过长会导致体验下降</p></td>
  </tr>
  <tr>
    <td><p>2、语句间隔可以用逗号隔开，例如“好的，打开空调”</p></td>
  </tr>
  <tr>
    <td><p>3、标点符号作用只有间隔作用，无法达到语气效果</p></td>
  </tr>
  <tr>
    <td><p>4、[=*]用于表示前一个汉字的指定拼音。
例如:
打开空调[=tiao2]
音调[=diao4]升高
其中，数字代表音调，支持1~5，5为轻声。</p></td>
  </tr>
  <tr>
    <td><p>5、[n*]用于表示为标记前的数字发音方式。
例如:
1300[n1]
1300[n2]
其中，n1指定为号码发音：一千三百；n2指定为数值发音：一三零零。</p></td>
  </tr>
  <tr>
    <td><p>6、“+”用于表示一条播报音被分成前后两段音频组合而成。
例如：
好的+空调已为您打开
好的+已关机
其中，“+”添加到句子中明显停顿的地方（如逗号、句号等处），合成的音频效果更为自然。
注意：每个命令词最多支持15段音频组合</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>播报模式</p></th>
  </tr>
  <tr>
    <td><p>1、播报模式分为两种：主动播报和被动播报。</p></td>
  </tr>
  <tr>
    <td><p>2、主动播报是指：语音系统识别到某个命令词时，播报对应的播报语句。</p></td>
  </tr>
  <tr>
    <td><p>3、被动播报是指：语音系统识别到某个命令词时，不进行任何播报；只有当接收到指定协议时才进行对应播报语句的播报。</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>发送协议</p></th>
  </tr>
  <tr>
    <td><p>发送协议是指：语音系统识别到某个命令词时，通过通信串口将该命令词对应的协议发送给上位机。</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>接收协议</p></th>
  </tr>
  <tr>
    <td><p>接收协议是指：语音系统通过串口接收某条协议时，系统播报协议对应的播报语句或处理协议对应的功能。</p></td>
  </tr>
</table>

<table>
  <tr>
    <th><p>其他隐藏功能</p></th>
  </tr>
  <tr>
    <td><p>1、如果命令词中存在音量控制相关的命令词，系统会自动实现对应的功能。如，命令词中存在“增大音量”或“减小音量”，当语音系统处于唤醒状态下并且识别到“增大音量”或“减小音量”时，语音系统会自动修改播报音量。</p></td>
  </tr>
  <tr>
    <td><p>2、如果某个命令词的识别不够灵敏，可在页面上更改该命令词的置信度阈值提高其识别灵敏度（非自动优化模式）；也可以增加同一语义的命令词以提高其识别泛化性</p></td>
  </tr>
</table>