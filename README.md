# IOTA Snapshot Recovery Tool

Using this tool you can move all your funds from a seed that has been used pre-snapshot to a new seed, for fixing the zero-balance problem.

The tool is completely secure, you run it on your own PC without anything being sent to the internet (well, except for the final transaction)

## How to use?

- Simply clone this repo.
- Run `npm install` to get the final dependencies.
- In the directory, run `node main.js <old seed> <new seed>`.
- Sit back and watch as the tool will find balances that are linked to your old seed.
- When you think you have all your balances, you simply hit the `i`-key and the final transaction is being made.

## How it works

The repository has a snapshot txt file in itself, this snapshot, at the time of writing, is the latest. If there is a newer snapshot you should replace the file on this repo with the newest.

The tool will then generate many different addresses based on your old seed, and compares locally with the snapshot file. If there is a hit (and assuming no money has been transferred after the snapshot period) the tool will include that address in 1 big transaction, along with the rest of the hits.

All the funds combined from the pre-snapshot addresses will be sent to a single address from the new seed, the new seed can now be reused as you would normally, with access to the full balance.

----

                                      .yNMmo           
                                     +MMMMM.          
              -+/` -yh+ .o+`          +hhy:           
             :MMMy /mNy +Nm-/dy `      ``.`           
              /ss.  `..   ` ./-:mo``  .dMMm: -shs-    
              .ydh- oMMs odh``-..`ho  .mNNN/ dMMMm    
        -yhy: :NNNo -ss- :s+`oNy./.    `::`  .oys-    
        hMMMN  .-.``   .-.  `.. :h/   :hdy.  -+/`     
        .+so:`   sdds -NMN.-mm+`::`   oNNm- -MMMh -++.
          `sddy. hNNh  /o: `/+..dd.  .-:-`  `/so.`NMMm
      ``  :NMMM/  ..    .`          -NMm.  +hh:   :oo-
    :hddy. -++:     -` /mh  PETER  `--/o/   smd/ /dd+  
    mMMMMy      ss -do `/+-  HI   +NN:  `yd+``  /dd+  
    :ydds.     -s: -yo  yMm`   `hh--- .:-sh/  yds``   
      ``       :y- -yo  `-://` `++`./.smo  ./-+y+     
               smo  odh`  dMM+     :y:``.+:+ds        
               .+/` :yo`  .:-.+o/     ys.s/ `         
                mNd   smm/   sMMM/    ``              
                .:::. +hh-`` `+o/ :ydh/               
                 .NMN-   /NNm-    hMMMm  .+o+.        
                  :+:`//./mNd- -/:.+s+. .NMMMN:       
                     mMMN.    yMMMm     `dMMMm.       
                     -ss/     /mMNo       .-.         
