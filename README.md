Reflektion over opgave.

Jeg har virkelig haft svært ved denne opgave, da jeg har følt at det var en meget stor opgave på lidt tid.

Kunne jeg starte forfra, ville jeg have startet mobile first og sikret responisviteten i sitet, men da jeg var bange for ikke at kunne nå at få sitet til at se ud som figma-filen, prioriterede jeg desktop.

Derudover, har jeg haft svært ved at nå at samle og rydde op i min kode navnligt css.

Der er helt klart mange ting jeg ville gøre anerledes, hvis jeg havde tiden. Dog har jeg gjort brug af variabler, pseudo elementer, data-surface og scroll-snap mm.

Nogle eksempler på dette:

[data-surface="gul"] {
    --bg-btn: var(--gul);
    --text-btn: var(--sort);
  }

  [data-surface="gul"]:hover {
    --bg-btn: var(--gul-hover);
    --text-btn: var(--sort);
  }

  [data-surface="hvid"] {
    --bg-btn: var(--hvid);
    --text-btn: var(--sort);
  }
  
  [data-surface="sort"] {
    --bg-btn: var(--sort);
    --text-btn: var(--hvid);
    
  }
  [data-surface="sort"]:hover {
    --bg-btn: var(--hvid);
    --text-btn: var(--sort);
    border: solid 2px var(--sort);
    
  }
  button {
    background: var(--bg-btn, var(--hvid));
    color: var(--text-btn, var(--sort));
    border-radius: 42px;
    padding: 16px 31px;
    font-family: var(--lato);
  }

  -------------------------------------------

  &::before {
        content: "";
        position: absolute;
        background: var(--grøn);
        top: 25px;
        left: 25px;
        width: 183px;
        height: 164px;
        border-radius: 12px;
        z-index: 1;
      }
      :first-of-type {
        position: absolute;
        top: 0;
        left: 0;
        width: 250px;
        height: 250px;
        object-fit: contain;
        z-index: 0;
      }

      :last-of-type {
        position: relative;
        z-index: 2;
        width: 450px;
        margin-left: 70px;
        margin-top: 20px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        border-radius: 12px;
      }




