# Hierarchical Planning for Long-Horizon Multi-Agent Collective Construction

<p style="text-align:center;">
<span style="background-color:#ffffd0;font-size:20px">
Accepted at ICRA 2024!
</span>
</p>


## Abstract
We develop a planner that directs robots to construct a 3D target structure composed of blocks. The robots themselves are cubes of the same size as the blocks, and they may place, carry, or remove one block at a time. When moving, robots are also allowed to climb or descend a block. A construction plan may thus build a staircase-like scaffolding of blocks to reach other blocks at higher levels. The order of block placement is important; for example, a block that sits atop other blocks must be placed after the blocks below it, and a block that needs scaffolding cannot be placed until after the scaffolding is. Prior works focus on end-to-end approaches that simultaneously plan for block placement order and inter-robot collisions. Larger structures are either intractable or yield high-cost solutions. A prior approach mitigates this by decomposing the structure into smaller components that can be planned for independently, but the computational challenge remains. We present a hierarchical approach that first (1) uses A* to determine a sequence of block placements and removals while ignoring inter-robot collision, then (2) identifies ordering constraints between block placement and removal actions, and finally (3) computes collision-free paths for multiple robots to perform said actions. Compared to an optimization approach that minimizes the number of timesteps to complete the structure, we observe a 100x reduction in computation time for comparable solutions.

## Supplementary Material for ICRA 2024 submission: Experiments and Results
### Test Structures
<table>
  <tr>
    <td align="center"><img src="large_structures_focal/large1.gif" alt="Structure 1" width="300"/></td>
    <td align="center"><img src="large_structures_focal/large2.gif" alt="Structure 2" width="300"/></td>
    <td align="center"><img src="large_structures_focal/large3.gif" alt="Structure 3" width="300"/></td>
      </tr>
  <tr>
    <td align="center"><img src="large_structures_focal/large4.gif" alt="Structure 4" width="300"/></td>
    <td align="center"><img src="large_structures_focal/large5.gif" alt="Structure 5" width="300"/></td>
    <td align="center"><img src="large_structures_focal/large6.gif" alt="Structure 6" width="300"/></td>
  </tr>
  <tr>
    <td align="center"><img src="large_structures_focal/large7.gif" alt="Structure 7" width="300"></td>
    <td align="center"><img src="large_structures_focal/large8.gif" alt="Structure 8" width="300"></td>
    <td align="center"><img src="large_structures_focal/large9.gif" alt="Structure 9" width="300"></td>
      </tr>
  <tr>
    <td align="center"><img src="large_structures_focal/large10.gif" alt="Structure 10" width="300"></td>
    <td align="center"><img src="large_structures_focal/large11.gif" alt="Structure 11" width="300"></td>
    <td align="center"><img src="large_structures_focal/large12.gif" alt="Structure 12" width="300"></td>
  </tr>
</table>

### Random Structures in Environment Size 7x7x4
<table>
  <tr>
    <td align="center"><img src="random_structures_focal/random0.gif" alt="Random Structure 0" width="250"></td>
    <td align="center"><img src="random_structures_focal/random1.gif" alt="Random Structure 1" width="250"></td>
    <td align="center"><img src="random_structures_focal/random2.gif" alt="Random Structure 2" width="250"></td>
    <td align="center"><img src="random_structures_focal/random3.gif" alt="Random Structure 3" width="250"></td>
    <td align="center"><img src="random_structures_focal/random4.gif" alt="Random Structure 4" width="250"></td>
    </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random5.gif" alt="Random Structure 5" width="250"></td>
    <td align="center"><img src="random_structures_focal/random6.gif" alt="Random Structure 6" width="250"></td>
    <td align="center"><img src="random_structures_focal/random7.gif" alt="Random Structure 7" width="250"></td>
    <td align="center"><img src="random_structures_focal/random8.gif" alt="Random Structure 8" width="250"></td>
    <td align="center"><img src="random_structures_focal/random9.gif" alt="Random Structure 9" width="250"></td>
    </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random10.gif" alt="Random Structure 10" width="250"></td>
    <td align="center"><img src="random_structures_focal/random11.gif" alt="Random Structure 11" width="250"></td>
    <td align="center"><img src="random_structures_focal/random12.gif" alt="Random Structure 12" width="250"></td>
    <td align="center"><img src="random_structures_focal/random13.gif" alt="Random Structure 13" width="250"></td>
    <td align="center"><img src="random_structures_focal/random14.gif" alt="Random Structure 14" width="250"></td>
  </tr>
  <tr>
    </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random15.gif" alt="Random Structure 15" width="250"></td>
    <td align="center"><img src="random_structures_focal/random16.gif" alt="Random Structure 16" width="250"></td>
    <td align="center"><img src="random_structures_focal/random17.gif" alt="Random Structure 17" width="250"></td>
    <td align="center"><img src="random_structures_focal/random18.gif" alt="Random Structure 18" width="250"></td>
    <td align="center"><img src="random_structures_focal/random19.gif" alt="Random Structure 19" width="250"></td>
    </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random20.gif" alt="Random Structure 20" width="250"></td>
    <td align="center"><img src="random_structures_focal/random21.gif" alt="Random Structure 21" width="250"></td>
    <td align="center"><img src="random_structures_focal/random22.gif" alt="Random Structure 22" width="250"></td>
    <td align="center"><img src="random_structures_focal/random23.gif" alt="Random Structure 23" width="250"></td>
    <td align="center"><img src="random_structures_focal/random24.gif" alt="Random Structure 24" width="250"></td>
    </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random25.gif" alt="Random Structure 25" width="250"></td>
    <td align="center"><img src="random_structures_focal/random26.gif" alt="Random Structure 26" width="250"></td>
    <td align="center"><img src="random_structures_focal/random27.gif" alt="Random Structure 27" width="250"></td>
    <td align="center"><img src="random_structures_focal/random28.gif" alt="Random Structure 28" width="250"></td>
    <td align="center"><img src="random_structures_focal/random29.gif" alt="Random Structure 29" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random31.gif" alt="Random Structure 31" width="250"></td>
    <td align="center"><img src="random_structures_focal/random32.gif" alt="Random Structure 32" width="250"></td>
    <td align="center"><img src="random_structures_focal/random33.gif" alt="Random Structure 33" width="250"></td>
    <td align="center"><img src="random_structures_focal/random34.gif" alt="Random Structure 34" width="250"></td>
    <td align="center"><img src="random_structures_focal/random35.gif" alt="Random Structure 35" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random36.gif" alt="Random Structure 36" width="250"></td>
    <td align="center"><img src="random_structures_focal/random37.gif" alt="Random Structure 37" width="250"></td>
    <td align="center"><img src="random_structures_focal/random38.gif" alt="Random Structure 38" width="250"></td>
    <td align="center"><img src="random_structures_focal/random39.gif" alt="Random Structure 39" width="250"></td>
    <td align="center"><img src="random_structures_focal/random40.gif" alt="Random Structure 40" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random41.gif" alt="Random Structure 41" width="250"></td>
    <td align="center"><img src="random_structures_focal/random42.gif" alt="Random Structure 42" width="250"></td>
    <td align="center"><img src="random_structures_focal/random43.gif" alt="Random Structure 43" width="250"></td>
    <td align="center"><img src="random_structures_focal/random44.gif" alt="Random Structure 44" width="250"></td>
    <td align="center"><img src="random_structures_focal/random45.gif" alt="Random Structure 45" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random46.gif" alt="Random Structure 46" width="250"></td>
    <td align="center"><img src="random_structures_focal/random47.gif" alt="Random Structure 47" width="250"></td>
    <td align="center"><img src="random_structures_focal/random48.gif" alt="Random Structure 48" width="250"></td>
    <td align="center"><img src="random_structures_focal/random49.gif" alt="Random Structure 49" width="250"></td>
    <td align="center"><img src="random_structures_focal/random50.gif" alt="Random Structure 50" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random52.gif" alt="Random Structure 52" width="250"></td>
    <td align="center"><img src="random_structures_focal/random53.gif" alt="Random Structure 53" width="250"></td>
    <td align="center"><img src="random_structures_focal/random54.gif" alt="Random Structure 54" width="250"></td>
    <td align="center"><img src="random_structures_focal/random55.gif" alt="Random Structure 55" width="250"></td>
    <td align="center"><img src="random_structures_focal/random56.gif" alt="Random Structure 56" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random57.gif" alt="Random Structure 57" width="250"></td>
    <td align="center"><img src="random_structures_focal/random58.gif" alt="Random Structure 58" width="250"></td>
    <td align="center"><img src="random_structures_focal/random59.gif" alt="Random Structure 59" width="250"></td>
    <td align="center"><img src="random_structures_focal/random60.gif" alt="Random Structure 60" width="250"></td>
    <td align="center"><img src="random_structures_focal/random61.gif" alt="Random Structure 61" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random62.gif" alt="Random Structure 62" width="250"></td>
    <td align="center"><img src="random_structures_focal/random63.gif" alt="Random Structure 63" width="250"></td>
    <td align="center"><img src="random_structures_focal/random64.gif" alt="Random Structure 64" width="250"></td>
    <td align="center"><img src="random_structures_focal/random65.gif" alt="Random Structure 65" width="250"></td>
    <td align="center"><img src="random_structures_focal/random66.gif" alt="Random Structure 66" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random67.gif" alt="Random Structure 67" width="250"></td>
    <td align="center"><img src="random_structures_focal/random68.gif" alt="Random Structure 68" width="250"></td>
    <td align="center"><img src="random_structures_focal/random69.gif" alt="Random Structure 69" width="250"></td>
    <td align="center"><img src="random_structures_focal/random70.gif" alt="Random Structure 70" width="250"></td>
    <td align="center"><img src="random_structures_focal/random71.gif" alt="Random Structure 71" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random72.gif" alt="Random Structure 72" width="250"></td>
    <td align="center"><img src="random_structures_focal/random74.gif" alt="Random Structure 73" width="250"></td>
    <td align="center"><img src="random_structures_focal/random75.gif" alt="Random Structure 75" width="250"></td>
    <td align="center"><img src="random_structures_focal/random76.gif" alt="Random Structure 76" width="250"></td>
    <td align="center"><img src="random_structures_focal/random77.gif" alt="Random Structure 77" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random78.gif" alt="Random Structure 78" width="250"></td>
    <td align="center"><img src="random_structures_focal/random79.gif" alt="Random Structure 79" width="250"></td>
    <td align="center"><img src="random_structures_focal/random80.gif" alt="Random Structure 80" width="250"></td>
    <td align="center"><img src="random_structures_focal/random81.gif" alt="Random Structure 81" width="250"></td>
    <td align="center"><img src="random_structures_focal/random82.gif" alt="Random Structure 82" width="250"></td>
    </tr>
  <tr>  
    <td align="center"><img src="random_structures_focal/random83.gif" alt="Random Structure 83" width="250"></td>
    <td align="center"><img src="random_structures_focal/random84.gif" alt="Random Structure 84" width="250"></td>
    <td align="center"><img src="random_structures_focal/random86.gif" alt="Random Structure 86" width="250"></td>
    <td align="center"><img src="random_structures_focal/random87.gif" alt="Random Structure 87" width="250"></td>
    <td align="center"><img src="random_structures_focal/random88.gif" alt="Random Structure 88" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random89.gif" alt="Random Structure 89" width="250"></td>
    <td align="center"><img src="random_structures_focal/random90.gif" alt="Random Structure 90" width="250"></td>
    <td align="center"><img src="random_structures_focal/random91.gif" alt="Random Structure 91" width="250"></td>
    <td align="center"><img src="random_structures_focal/random93.gif" alt="Random Structure 92" width="250"></td>
    <td align="center"><img src="random_structures_focal/random94.gif" alt="Random Structure 94" width="250"></td>
  </tr>
  <tr>
    <td align="center"><img src="random_structures_focal/random95.gif" alt="Random Structure 95" width="250"></td>
    <td align="center"><img src="random_structures_focal/random96.gif" alt="Random Structure 96" width="250"></td>
    <td align="center"><img src="random_structures_focal/random97.gif" alt="Random Structure 97" width="250"></td>
    <td align="center"><img src="random_structures_focal/random98.gif" alt="Random Structure 98" width="250"></td>
    <td align="center"><img src="random_structures_focal/random99.gif" alt="Random Structure 99" width="250"></td>
  </tr>
</table>
