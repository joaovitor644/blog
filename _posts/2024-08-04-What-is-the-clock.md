---
layout: post
title: O que è um Clock?
description: Trabalho de Sistemas Digitais relacionado a Sinais de Relógio (clock)
tags:
  - Sistemas_Digitais
Fonts: Wikipédia
---


Em sistemas digitais, é fundamental que haja um controle do fluxo das informações para garantir que as informações estejam disponíveis no momento correto nos circuitos digitais, especialmente circuitos mais complexos. Para garantir isso é necessário sincronizar as operações dos sistemas usando algum tipo de referencial, como um pulso , o que é garantido através de um clock.

Um clock pode ser considerado uma métrica de velocidade de operações que um processador pode executar , mas também é um componente eletrônico capaz de sincronizar dois ou mais circuitos eletrônicos através de pulsos elétricos de alta voltagem ou de baixa voltagem, (ou seja , alternado entre os sinais lógicos 0 e 1) tornado os circuitos síncronos.

  
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdj9RYAlEj8qPncmM2e0y5wLe735CaWivR-0GE1El9o-VWf-s_kyS2U0CZH5VWxG5gMkLnr49crdAA2Uw-ZREaq0u5HEr_cL67LhnHhGhj_CFCoSbbk_DR3CA4hVWXiRUpVYe-7CnkOHVlH9G8knVzy61Fr?key=fJd0peSDsd8nPIe_BCNePA)  
Imagem de um Cristal e [](https://pt.wikipedia.org/wiki/Circuito_integrado)Circuito integrado gerador de frequência (clock)
fonte:Wikipédia

  

A métrica utilizada para determinar a frequência de um clock é chamada de Hertz (Hz) (ciclos por segundo), sendo que 1 Hz é equivalente a uma pulsação por segundo e essa medida é definida pela relação entre frequência e Período (T) dada por:


  f = 1T

Um período é o tempo que o sinal de alta voltagem (sinal lógico 1) permanece ativo em cada pulso de clock. Por exemplo:  em um pulso de clock é possível que seja ajustado para que 50% do tempo de uma pulsação permaneça com o sinal de voltagem alta, ou seja se meu clock trabalha com frequência  1 Hz e período de 50%  então em 0.5s o sinal do clock permanece em voltagem alta, se fosse em um período de 30% então ele permaneceria em 0.3s.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJpwmbiS9pu6shv8Bw_fNxwseXykQgF9NFyOuuuItpWkj6nMbOfcT3Bvql9vPCnhOCr8iggQd7mVP8EpOAyCk7jj_M0k72ZX8BKl1v_b5alDewcMaTWJ6J6RYVdjNbyEM1jVjAN3ix5A0HluDiOYvwOf8?key=fJd0peSDsd8nPIe_BCNePA)

Atualmente com os avanços da tecnologia, principalmente em processadores, os circuitos de  clock tiveram avanços significativos em relação a sua frequência podendo ter a capacidade de 5 GHz (5 bilhões de ciclos em um único segundo) ou mais. Além de manter os circuitos sincronizados , o clock é fundamental para a execução de instruções de uma máquina e a transferência de dados.

| Frequência |          Ciclos/Seg          | Período |
| :--------: | :--------------------------: | :-----: |
|    1Hz     |       1 ciclo/segundo        |   1s    |
|    10Hz    |      10 ciclos/segundo       |  0.1s   |
|   100Hz    |      100 ciclos/segundo      |  0.01s  |
|    1KHz    |     1000 ciclos/segundo      |   1ms   |
|    1MHz    |   1,000,000 ciclos/segundo   |   1μs   |
|    1GHz    | 1,000,000,000 ciclos/segundo |   1ns   |

Tabela de frequências 


## Evolução Da frequência dos Circuitos de clock


A evolução da frequência de clock acompanha há muitos anos a evolução dos processadores uma vez que para que o processador faça o seu papel corretamente e de maneira precisa e sincronizada com o circuito , é necessário o uso de clock e a partir do momento em  que os computadores necessitam evoluir no quesito velocidade , foi necessário que não só os processadores tivessem um poder enorme de processamento como também que eles processassem mais rápido.

  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXckbZ8DvBlBZwom_-rqZBdYR0-m530o56SRRagez29U4QaCnXNEGIGJ4APqdTl20_LlCxLbDJAq_D4kp2ohOAkwUAf6MMbZA2-3tk1bhGI6amQMw5JUA3rGKThxrMaNhKy8ng3aSrQyKMF_u6oD2zBYC-Sf?key=fJd0peSDsd8nPIe_BCNePA)

Intel 4004 foi o primeiro microprocessador da história (Fonte da imagem: [Wikimedia Commons](http://commons.wikimedia.org))

  

Tudo começou com o microprocessador Intel 4004 em 1971 com o clock máximo de 740 KHz podendo calcular até 92 mil instruções por segundo. A partir de seu sucesso foi lançado o Intel 8008 em 1972 com 0.8 MHz de frequência máxima , e logo mais adiante esse modelo foi substituído pelo Intel 8080 em 1974. com um limite de clock de 2 MHz , o que era muito alto para a época. Desde então a produção e evolução dos processadores foi crescendo exponencialmente assim como as frequências de clock, até chegarmos no ponto onde os processadores possuem o tamanho dos seus transistores diminuído significativamente, tornando um desafio aumentar a frequência do clock devido a limitações físicas. Diante disso, para contornar esse problema foi o uso de mais de um núcleo ao mesmo tempo, através da tecnologia multicore possibilitando que cada núcleo não precise de uma frequência alta para funcionar , como por exemplo o processador Dual-Core de 1.5GHz que consegue ter um desempenho semelhante a um processador de 1 núcleo com frequência de de 3 GHz.


## Estado de Metaestabilidade
  

Todos os flip flops , em sistemas digitais possuem requisitos de Tempo bem definidos que permitem que cada flip  flop capture corretamente um dado de sua entrada e produza um sinal de saída. Para garantir isso , o dado de entrada de um flip flop deve estar estável por um tempo mínimo antes da borda do clock e por um tempo mínimo depois da borda do clock para então a saída do flip flop ser disponibilizada depois de um tempo específico de atraso de propagação de sinal. Se um dado de entrada viola os requisitos de tempo mínimo de borda , então o flip flop se torna instável. Esse Estado do flip flop é conhecido como estado de metaestabilidade. No estado de metaestabilidade, a saída do flip flop pode flutuar entre os estados lógicos alto e baixo por um tempo indeterminado, o que significa que a transição para um estado lógico definido alto ou baixo é maior que o tempo de propagação de sinal.

 ![Metaestabilidade representada como uma bola liberada em uma colina](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcPzML66-Yl5QtxZuTeKRVD9X6E18XG6YYBKFuhdlWw1mrSaVQWpnSwWqLBzftwYqohXW9kDz56TuNduv8EaI94fFqEkduKdAlAuyMWkG5IlxeaBMn4jpbVm75CaFtZmLVwJxcjzVItEHRTsE2nyrG-59Q?key=fJd0peSDsd8nPIe_BCNePA)
Metaestabilidade representada como uma bola liberada em uma colina, Fonte:[Understanding Metastability in FPGAs – Altera (Intel) White Paper](https://www.altera.com/en_US/pdfs/literature/wp/wp-01082-quartus-ii-metastability.pdf)

  

Em sistemas síncronos, os sinais de entrada devem respeitar os tempos mínimos de borda para que não ocorra problema de metaestabilidade que ocorre quando um sinal de clock é transferido entre circuitos de domínios de clock distintos ou transferências de um sistema assíncrono para um sistema síncrono. Durante uma transferência de um dado de um flip flop em metaestabilidade para outro vai para um estado lógico antes do flip flop capturar , não há nenhum impacto na transferência, entretanto , se não for para em um estado lógico válido antes da captura do flip flop pode ocorrer uma falha no sistema. Uma forma de resolver esse problema é utilizado uma sequência de flip flops no domínio do clock de destino para ressincronizar o sinal no novo domínio clock permitindo um tempo extra  para que o sinal potencialmente  metaestável assuma um nível lógico estável antes de ser utilizado na lógica do sistema digital.

![metaestabilidade-figura3](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf_kpcEXASunkOqbwctbENOpUQrHpCGaHa8CaA3NqJlWkiF2m5V0KHioxbOWaBk6RhKKZkMcDnYWpUX55n3aN9wt--waao27psubWS2vX7ZzhAC8GBnAE_kspzfxPOvN_h-6MRfINPS4-k_7dbXXRlZ5AU3?key=fJd0peSDsd8nPIe_BCNePA)  

  
  
  
  

Referências

---

 Manual do Código. Curso Assembly (SNES e Mega Drive) - Parte 7. Disponível em: <https://www.manualdocodigo.com.br/curso-assembly-snes-mega-parte7/>. Acesso em: 04 out. 2023.

Wiki IFPR. Clock. Disponível em: <https://wiki.foz.ifpr.edu.br/wiki/index.php/Clock>. Acesso em: 04 out. 2023.

Wikipedia. Sinal de Relógio. Disponível em: <https://pt.wikipedia.org/wiki/Sinal_de_rel%C3%B3gio>. Acesso em: 04 out. 2023.

 Dicionário Técnico. Sinal de Relógio (Clock). Disponível em: <https://dicionariotec.com/posts/sinal-de-relogio-clock>. Acesso em: 04 out. 2023.

TechTudo. O que é o Clock do PC: conheça o indicador de performance em CPUs. Disponível em: <https://www.techtudo.com.br/noticias/2022/07/o-que-e-o-clock-do-pc-conheca-o-indicador-de-performance-em-cpus.ghtml>. Acesso em: 04 out. 2023.

Embarcados. Metaestabilidade. Disponível em: <https://embarcados.com.br/metaestabilidade/#O-que-e-metaestabilidade>. Acesso em: 04 out. 2023.

 TecMundo. A História dos Processadores. Disponível em: 
<https://www.tecmundo.com.br/historia/2157-a-historia-dos-processadores.htm>. Acesso em: 04 out. 2023.
