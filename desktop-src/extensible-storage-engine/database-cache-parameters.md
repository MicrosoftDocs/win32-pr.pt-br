---
description: 'Saiba mais sobre: Parâmetros de cache de banco de dados'
title: Parâmetros de cache do banco de dados
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: defc33e3d020b9a6b59c580446afc51ee12631a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476661"
---
# <a name="database-cache-parameters"></a>Parâmetros de cache do banco de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="database-cache-parameters"></a>Parâmetros de cache do banco de dados

Este tópico contém parâmetros que são usados para o cache do banco de dados.

*JET_paramBatchIOBufferMax*  
22  

Esse parâmetro controla o tamanho de uma parte auxiliar do cache de página do banco de dados que é usada para simular a E/S de coleta de dispersão quando ela não estiver disponível. O tamanho está nas páginas do banco de dados.

**Windows XP e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>256</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0, 2 – 2147483647</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSize*  
41  

Esse parâmetro pode ser usado para controlar o tamanho do cache de página do banco de dados em tempo de executar. Normalmente, o cache ajustará automaticamente seu tamanho como uma função dos níveis de atividade do banco de dados e do computador. Se o aplicativo define esse parâmetro como zero, o cache ajustará seu próprio tamanho dessa maneira. No entanto, se o aplicativo define esse parâmetro como um valor não zero, o cache se ajustará ao tamanho de destino (nas páginas do banco de dados). Em seguida, o cache manterá seu tamanho nesse limite até receber um novo tamanho ou até que seja liberado para escolher seu próprio tamanho.

**Observação**  O tamanho do cache ainda está sujeito aos limites impostos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

Quando esse parâmetro é lido, o tamanho real do cache nas páginas do banco de dados é retornado. Esse tamanho pode ser usado pelo aplicativo como uma entrada para impulsionar seu ajuste manual do tamanho do cache.


| | | <p>Valor padrão:</p> | <p>Especial</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSizeMin*  
60  

Esse parâmetro configura o tamanho mínimo do cache de página do banco de dados. O tamanho está nas páginas do banco de dados.

Por padrão, o cache do banco de dados ajustará automaticamente seu tamanho entre os limites definidos **por JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Windows 2000:**  No Windows 2000, esse parâmetro deve ser definido como um valor aproximadamente igual a quatro vezes o número de threads que estarão dentro da API do ESE ao mesmo tempo. Isso é necessário para evitar deadlocks causados por um número insuficiente de buffers de cache de página de banco de dados para executar operações complexas, como divisão de árvore B+.

**Windows XP e posterior:**  O gerenciador de cache definirá automaticamente seu próprio tamanho mínimo de cache para evitar deadlocks.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows XP:</strong> 1</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSizeMax*  
23  

Esse parâmetro configura o tamanho máximo do cache de página do banco de dados. O tamanho está nas páginas do banco de dados.

Por padrão, o cache do banco de dados ajustará automaticamente seu tamanho entre os limites definidos **por JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Observação**   Se esse parâmetro for deixado com seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando [JetInit](./jetinit-function.md) for chamado.

**Windows Vista:**  A partir Windows Vista, o valor padrão desse parâmetro foi alterado para esclarecer esse comportamento.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 512</p><p><strong>Windows Vista:</strong> 200000000</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p><strong>Windows XP e Windows 2000:</strong>  Não</p><p><strong>Windows Vista e Windows Server 2003:</strong>  Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCheckpointDepthMax*  
24 

Esse parâmetro controla como as páginas de banco de dados são liberadas agressivamente do cache de página do banco de dados para minimizar a quantidade de tempo que levará para se recuperar de uma falha. O parâmetro é um limite em bytes para saber quantos arquivos de log de transações precisarão ser reprodução após uma falha.

Se o log circular estiver habilitado usando [JET_paramCircularLog,](./transaction-log-parameters.md) esse parâmetro também controlará a quantidade aproximada de arquivos de log de transações que serão retidos no disco.

É importante que esse parâmetro não seja definido como muito baixo. À medida que o valor desse parâmetro se aproximar de zero, o cache se tornará cada vez mais agressivo ao liberar páginas de banco de dados para o disco. Isso não só resulta em um número maior de gravações nos arquivos de banco de dados, mas também causa indiretamente um número maior de leituras para esses arquivos também. Isso pode causar problemas de desempenho muito significativos em alguns casos. Infelizmente, definir o menor valor ideal para esse parâmetro só pode ser feito usando experimentação com o aplicativo de destino.


| | | <p>Valor padrão:</p> | <p>20971520</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | | <p>Escopo:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Esse parâmetro é global.</p><p><strong>Windows Vista:</strong>  Esse parâmetro é por instância.</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCheckpointIOMax*  
135  

Esse parâmetro controla o número máximo de gravações simultâneas que o mecanismo de banco de dados usará para liberar páginas de banco de dados modificadas com a finalidade de avançar o ponto de verificação. O valor desse parâmetro pode ser usado para equilibrar a velocidade com a qual o ponto de verificação pode ser avançado versus o impacto negativo que esse processo terá no tempo de resposta para outras operações de E/S para os discos que contém o banco de dados.


| | | <p>Valor padrão:</p> | <p>96</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>8 – 1024</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramEnableViewCache*  
127  

Quando esse parâmetro for **True**, o mecanismo de banco de dados usará dados de banco de dados diretamente do cache de arquivos Windows em vez de copiar os dados armazenados em cache em sua própria memória privada. Todos os dados de banco de dados modificados ainda serão armazenados em cache na memória privada.

A intenção desse modo é reduzir ainda mais a quantidade de memória privada usada pelo mecanismo de banco de dados para armazenar em cache os dados do banco de dados.

O cache de exibição só poderá ser usado se o uso do cache Windows arquivo estiver habilitado definindo JET_paramEnableFileCache como **True.**


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramLRUKCorrInterval*  
25  

Esse parâmetro define o intervalo de tempo em microssegundos nos quais dois acessos de página de banco de dados são considerados correlacionados. Esse intervalo de correlação controla a sensibilidade do LRU-K (algoritmo de substituição de página) do cache para acessos sucessivos de página. Isso, por sua vez, afetará quais páginas ele escolhe manter armazenadas em cache.


| | | <p>Valor padrão:</p> | <p>128000</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKHistoryMax*  
26  

Esse parâmetro define o número máximo de páginas de banco de dados não armazenadas em cache para as quais os tempos de acesso à página do banco de dados serão mantidos. Esses registros de histórico permitem que o LRU-K (algoritmo de substituição de página) do cache detecte com mais precisão páginas populares que foram despejadas incorretamente do cache de página do banco de dados.

**Windows XP e Windows Server 2003:**  Esse parâmetro é ignorado no Windows XP e Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong> 1024</p><p><strong>Windows Vista:</strong> 100000</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 0 – 4194303</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKPolicy*  
27  

Esse parâmetro configura o número de acessos de página de banco de dados que são considerados para determinar a utilidade da página. Esse parâmetro é essencialmente o K em LRU-K, o algoritmo de substituição de página do cache de página do banco de dados.


| | | <p>Valor padrão:</p> | <p>2</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1-2</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKTimeout*  
28

Esse parâmetro indica o período de tempo em segundos após o qual uma página no cache de página do banco de dados é considerada perdida um acesso à página com a finalidade de considerar a utilidade da página.


| | | <p>Valor padrão:</p> | <p>100</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 1 – 2147483647</p><p><strong>Windows Vista:</strong> 1 a 4294967295</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKTrxCorrInterval*  
29  

Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

*JET_paramStartFlushThreshold*  
31  

Esse parâmetro controla quando o cache de página do banco de dados começa a remover páginas do cache para liberar espaço para páginas que não são armazenadas em cache. Quando o número de buffers de página no cache cair abaixo desse limite, um processo em segundo plano será iniciado para reabastecer o pool de buffers disponíveis. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por **JET_paramCacheSizeMax**. Esse limite também deve ser menor que o limite de parada definido por **JET_paramStopFlushThreshold**.

A altura da distância do limite inicial determinará o tempo de resposta que o cache da página do banco de dados deve ter para produzir os buffers disponíveis antes que o aplicativo precise deles. Um limite de início alto dará ao processo em segundo plano mais tempo para reagir. no entanto, um limite de início alto implica um limite de parada maior e reduzirá o tamanho efetivo do cache de página de banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 5 (1%)</p><p><strong>Windows Vista:</strong> 20 milhões (1%)</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramStopFlushThreshold*  
32  

Esse parâmetro controla quando o cache da página do banco de dados encerra a remoção de páginas do cache para liberar espaço para páginas que não são armazenadas em cache. Quando o número de buffers de página no cache ultrapassar esse limite, o processo em segundo plano que foi iniciado para reabastecer o pool de buffers disponíveis será interrompido. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por **JET_paramCacheSizeMax**. Esse limite também deve ser maior que o limite de início definido por **JET_paramStartFlushThreshold**.

A distância entre o limite inicial e o limite de interrupção afeta a eficiência com a qual as páginas de banco de dados são liberadas pelo processo em segundo plano. Um intervalo maior fará com que seja mais provável que as gravações nas páginas vizinhas possam ser combinadas. no entanto, um limite de parada alta reduzirá o tamanho efetivo do cache de página de banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 10 (2%)</p><p><strong>Windows Vista:</strong> 40 milhões (2%)</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
