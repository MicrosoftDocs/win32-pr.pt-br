---
title: otimizando o desempenho de DVD para jogos de Windows
description: este artigo discute como otimizar o desempenho de DVD para jogos de Windows.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe08ba6188df9b8bbc25a73595bf1509b257696955c1fcbd1ae98091b3c8aecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042527"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>otimizando o desempenho de DVD para jogos de Windows

uma alta porcentagem de computadores que executam Windows ter uma unidade de DVD e muitos jogos são fornecidos em dvd. Como resultado, recomendamos que você garanta que seus jogos usem a unidade de DVD para sua total vantagem. Ao entender como os dados são lidos de um DVD e como o local dos dados afeta seu tempo de leitura, você pode reduzir os tempos de carregamento e melhorar o desempenho geral durante o jogo. este artigo discute como otimizar o desempenho de DVD para jogos de Windows.

-   [Layout básico de um DVD](#basic-layout-of-a-dvd)
-   [Lendo de um DVD](#reading-from-a-dvd)
-   [Lendo erros](#reading-errors)
-   [Taxa de transferência de dados](#data-throughput)
-   [Exemplos de taxa de transferência desperdiçada](#examples-of-wasted-throughput)
-   [Lendo de forma síncrona versus assíncrona](#reading-synchronously-vs-asynchronously)
-   [Lendo de forma ideal](#reading-optimally)
-   [Compatibilidade com DVD](#dvd-compatibility)
-   [Resumo](#summary)

## <a name="basic-layout-of-a-dvd"></a>Layout básico de um DVD

Esta figura mostra o layout básico de um DVD.

![layout do DVD](images/dvdsector.png)

Os dados em um DVD são armazenados como uma espiral contínua, como em um CD; no entanto, os arquivos são divididos em blocos e setores. Os arquivos são distribuídos por blocos ECC (código de correção de erro) e cada bloco é dividido em setores de 16 2 KB (ou seja, 32 KB de dados em cada bloco). Os arquivos são alinhados ao longo dos limites do setor e qualquer espaço não utilizado em um setor é deixado vazio. Se um arquivo tiver apenas 10 bytes, o restante do espaço nesse setor de 2 KB será desperdiçado; assim, quando possível, agrupar arquivos em incrementos de 2 KB para obter a melhor densidade de dados. Lembre-se de que essas especificações são apenas para DVD, e CD e HD-DVD têm especificações diferentes.

## <a name="reading-from-a-dvd"></a>Lendo de um DVD

Esta é a sequência que uma unidade de DVD executa após receber uma solicitação de leitura de um DVD:

1.  Alterar as camadas, se necessário
2.  Seek
3.  Refocar a OPU (unidade de retirada óptica) para ler os dados
4.  Verificar a posição real
5.  Ajustar e repetir até que os dados corretos sejam encontrados

As operações de leitura de unidade são quantificadas de forma diferente, dependendo se são leituras de unidade lógica ou leituras de unidade física. Leituras de unidade lógica só podem ler uma quantidade inteira de setores de DVD, enquanto uma solicitação de leitura de unidade física só pode ler uma quantidade inteira de blocos ECC. Normalmente, a unidade física recebe uma solicitação de leitura; Ele tentará preencher seu cache. O tamanho do cache da unidade de DVD depende das especificações da unidade individual.

Quando uma unidade de DVD recebe uma solicitação de leitura que excede o tamanho do cache, a solicitação é dividida em solicitações de tamanho de cache. A unidade procura o bloco ECC que contém o primeiro setor da solicitação e lê o bloco ECC inteiro. O firmware da unidade decodifica o bloco ECC e, em seguida, lê o próximo bloco ECC. O processo é repetido até que o cache da unidade seja preenchido ou todas as solicitações sejam atendidas. Em seguida, o kernel lê os dados decodificados do cache da unidade. Em seguida, ele libera o cache e inicia a próxima operação de leitura, se as solicitações de leitura permanecerem.

> [!Note]  
> Cada leitura não armazenada em cache libera o cache da unidade.

 

## <a name="reading-errors"></a>Lendo erros

DVDs e unidades de DVD não são perfeitos e podem ocorrer erros durante a leitura. Como CDs, partes de um DVD podem se tornar ilegíveis ou arranhões. Se qualquer parte de um bloco for ilegível, o bloco inteiro será considerado ilegível. Se ocorrer um erro de leitura, a unidade tentará ler novamente o bloco ECC. Se o bloco ainda estiver ilegível, a unidade anulará a operação de leitura e retornará um valor para o kernel que indica que o bloco estava ilegível. O kernel decide qual etapa deve ser tomada em seguida. O kernel pode reemitir a solicitação, anular a leitura completamente ou girar a unidade para baixo e emitir novamente a solicitação.

## <a name="data-throughput"></a>Taxa de Transferência de Dados

A taxa de transferência de dados de uma unidade de DVD depende de vários fatores: o local dos dados solicitados, a limpeza ou o rabisco do disco, o número de fluxos que estão sendo lidos do disco, o tamanho dos buffers associados a esses fluxos e as especificações da unidade individual. A taxa de transferência também depende se a unidade tem velocidade angular constante (CAV) ou velocidade linear constante (CLV). Se uma unidade for girada com CAV, o disco gira na mesma velocidade, independentemente de onde a unidade de retirada óptica (OPU) está localizada. Isso significa que o controle de dados passa para o OPU mais rápido à medida que o OPU fica mais próximo da borda externa do disco. Com o CLV, o disco gira mais lentamente à medida que o OPU se move para fora, portanto, o controle de dados passa para a OPU em uma velocidade constante. As unidades de DVD na maioria dos computadores usam CLV.

Enquanto a unidade está buscando e alterando camadas, os dados não podem ser lidos do disco. É uma boa prática minimizar essas operações, especialmente ao ler dados para uma tela de carregamento inicial.

## <a name="examples-of-wasted-throughput"></a>Exemplos de taxa de transferência desperdiçada

Para entender como a taxa de transferência de dados pode ser desperdiçada, considere uma unidade hipotética e um DVD. Vamos supor que um arquivo no meio do disco precisa ser lido. A taxa de transferência dessa área do disco é de aproximadamente 8,25 MB/s. Se o traço de busca for uma metade ou um terço de completo, o tempo médio de busca será de 150 ms. Neste exemplo, 1,2 MB (150 ms × 8,25 MB/s) podem ter sido lidos no momento em que levou apenas para obter o OPU para onde ele possa ler. A adição de uma alteração de camada gera a taxa de transferência desperdiçada para 1,8 MB (225 MS × 8,25 MB/s).

Outro exemplo que demonstra uma taxa de transferência desperdiçada é o carregamento de 20 arquivos mal localizados de uma unidade CAV sem alterações de camada. Se o tempo de busca de cada arquivo, mais a latência antes que os dados possam ser lidos, for de aproximadamente 200 MS, então 4 segundos (20 arquivos × 200 MS) serão gastos apenas para procurar os dados. Se os arquivos estiverem localizados no diâmetro externo e forem lidos em 11 × velocidade, a média da taxa de transferência será de 15,2 MB/s (11 velocidade/12 velocidade × 16 MB/s). A taxa de transferência desperdiçada neste exemplo é de aproximadamente 60,8 MB (15,2 MB/s × 4 s).

## <a name="reading-synchronously-vs-asynchronously"></a>Lendo de forma síncrona versus assíncrona

A leitura assíncrona é mais eficiente do que a leitura síncrona. Ao ler de forma síncrona, um ou mais blocos de dados ECC são lidos na memória do sistema antes de serem copiados para a memória do aplicativo. Por outro lado, a leitura assíncrona copia blocos ECC decodificados diretamente para a memória do aplicativo, o que evita o cache L2 e cria menos sobrecarga de CPU. Para ler de forma assíncrona, use o sinalizador de sinalizador de arquivo \_ \_ sobreposto ao usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir arquivos. A função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) também precisa de uma estrutura OVERLAPPED válida passada para executar e/s assíncrona.

Mais informações sobre e/s assíncronas podem ser encontradas em [e/s síncrona e](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o)síncrona.

## <a name="reading-optimally"></a>Lendo de forma ideal

O melhor princípio na leitura de um DVD é evitar a busca e a leitura de pequenas quantidades de dados. Quando a quantidade de dados lido é menor que a capacidade de um bloco ECC — menos de 32 KB – o restante do bloco é desperdiçado. Como os tamanhos de cache variam de drive para unidade, os desenvolvedores devem decidir uma quantidade mínima de dados para solicitações de leitura e não fazer nenhum menor. O tamanho mínimo deve ser um inteiro múltiplo de um bloco de ECC para evitar desperdício de tempo na leitura e decodificação de dados que não serão usados. Também é importante evitar a busca de todos os custos, pois qualquer tempo gasto em busca é o tempo gasto não lendo os dados.

## <a name="dvd-compatibility"></a>Compatibilidade com DVD

Há alguns problemas de compatibilidade importantes a serem considerados durante a liberação em DVD. primeiro, as unidades de DVD em computadores baseados em Windows podem variar em desempenho, portanto, se o DVD tiver um requisito específico para a taxa de transferência, é importante garantir que o hardware dos usuários atenda a esses requisitos. Além disso, os DVDs multicamadas podem causar problemas de compatibilidade em algumas unidades de DVD. Para evitar esses problemas, é aconselhável entregar um DVD de camada única ou testar exaustivamente um DVD de várias camadas em uma maioria das unidades antes do lançamento.

## <a name="summary"></a>Resumo

Para melhorar o desempenho do DVD, algumas regras gerais podem ser aplicadas. As técnicas a seguir podem ajudar a maximizar a taxa de transferência e reduzir os dados desperdiçados:

-   Evite leituras menores que 32 KB
-   Dispor dados para reduzir ou eliminar buscas
-   Dispor dados em limites de bloco ECC
-   Maximize a capacidade agrupando arquivos pequenos em blocos de 2 KB e reduza o espaço de preenchimento em setores de DVD
-   Leitura assíncrona para reduzir a carga da CPU e o uso excessivo de memória
-   Evite liberar DVDs multicamadas

 

 