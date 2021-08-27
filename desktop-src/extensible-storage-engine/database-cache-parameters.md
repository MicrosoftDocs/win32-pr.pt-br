---
description: 'Saiba mais sobre: parâmetros de cache de banco de dados'
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
ms.openlocfilehash: 43d51be7e2db82d64c70f6fa810be3caf4c6fbd8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984089"
---
# <a name="database-cache-parameters"></a>Parâmetros de cache do banco de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="database-cache-parameters"></a>Parâmetros de cache do banco de dados

Este tópico contém parâmetros que são usados para o cache de banco de dados.

*JET_paramBatchIOBufferMax*  
22  

Esse parâmetro controla o tamanho de uma parte auxiliar do cache de página de banco de dados que é usado para simular e/s de dispersão, quando ele não está disponível. O tamanho está em páginas de banco de dados.

**Windows XP e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>256</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>0, 2 – 2147483647</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSize*  
41  

Esse parâmetro pode ser usado para controlar o tamanho do cache de página do banco de dados em tempo de execução. Normalmente, o cache ajustará automaticamente seu tamanho como uma função de níveis de atividade de banco de dados e máquina. Se o aplicativo definir esse parâmetro como zero, o cache ajustará seu próprio tamanho dessa maneira. No entanto, se o aplicativo definir esse parâmetro como um valor diferente de zero, o cache se ajustará a esse tamanho de destino (em páginas de banco de dados). O cache manterá seu tamanho nesse limite até que um novo tamanho seja fornecido ou até que seja liberado para escolher seu próprio tamanho.

**Observação**  O tamanho do cache ainda está sujeito aos limites impostos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

Quando esse parâmetro é lido, o tamanho real do cache nas páginas do banco de dados é retornado. Esse tamanho pode ser usado pelo aplicativo como uma entrada para orientar seu ajuste manual do tamanho do cache.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Especial</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSizeMin*  
60  

Esse parâmetro configura o tamanho mínimo do cache de página do banco de dados. O tamanho está em páginas de banco de dados.

Por padrão, o cache de banco de dados ajustará automaticamente seu tamanho entre os limites definidos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Windows 2000:**  no Windows 2000, esse parâmetro deve ser definido como um valor aproximadamente igual a quatro vezes o número de threads que estarão dentro da API ESE ao mesmo tempo. Isso é necessário para evitar deadlocks causados por um número insuficiente de buffers de cache de página de banco de dados para executar operações complexas, como divisões de árvore B +.

**Windows XP e posterior:**  O Gerenciador de cache definirá automaticamente seu próprio tamanho mínimo de cache para evitar deadlocks.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong> 64</p><p><strong>Windows XP:</strong> 1</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Ok</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Ok</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCacheSizeMax*  
23  

Esse parâmetro configura o tamanho máximo do cache de página do banco de dados. O tamanho está em páginas de banco de dados.

Por padrão, o cache de banco de dados ajustará automaticamente seu tamanho entre os limites definidos por **JET_paramCacheSizeMin** e **JET_paramCacheSizeMax**.

**Observação**   Se esse parâmetro for deixado para seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando [JetInit](./jetinit-function.md) for chamado.

**Windows Vista:**  a partir do Windows Vista, o valor padrão desse parâmetro foi alterado para esclarecer esse comportamento.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 512</p><p><strong>Windows Vista:</strong> 2000000000</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000:</strong>  Não</p><p><strong>Windows XP:</strong>  Ok</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows XP e Windows 2000:</strong>  Não</p><p><strong>Windows Vista e Windows Server 2003:</strong>  Ok</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCheckpointDepthMax*  
24 

Esse parâmetro controla o quão agressivamente as páginas do banco de dados são liberadas do cache de página do banco de dados para minimizar a quantidade de tempo que levará para se recuperar de uma falha. O parâmetro é um limite em bytes para saber quantos arquivos de log de transações deverão ser reproduzidos após uma falha.

Se o log circular estiver habilitado usando [JET_paramCircularLog](./transaction-log-parameters.md) , esse parâmetro também controlará a quantidade aproximada de arquivos de log de transações que serão retidos no disco.

É importante que esse parâmetro não seja definido como muito baixo. Como o valor desse parâmetro se aproxima de zero, o cache se tornará cada vez mais agressivo ao liberar páginas de banco de dados para o disco. Isso não apenas resulta em um número maior de gravações nos arquivos de banco de dados, mas também causa indiretamente um número maior de leituras nesses arquivos. Isso pode causar problemas de desempenho muito significativos em alguns casos. Infelizmente, definir o menor valor ideal para esse parâmetro só pode ser feito usando experimentação com o aplicativo de destino.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>20971520</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | 
| <p>Escopo:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> Esse parâmetro é global.</p><p><strong>Windows Vista:</strong>  Esse parâmetro é por instância.</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Sim</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCheckpointIOMax*  
135  

Esse parâmetro controla o número máximo de gravações simultâneas que o mecanismo de banco de dados usará para liberar páginas de banco de dados modificadas com a finalidade de avançar o ponto de verificação. O valor desse parâmetro pode ser usado para balancear a velocidade com a qual o ponto de verificação pode ser avançado versus o impacto negativo que esse processo terá no tempo de resposta para outras operações de e/s nos discos que contêm o banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>96</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>8 a 1024</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramEnableViewCache*  
127  

quando esse parâmetro for **True**, o mecanismo de banco de dados usará os bancos de dado diretamente do cache de arquivos Windows em vez de copiar os dados armazenados em cache em sua própria memória privada. Qualquer dado de banco de dados modificado ainda será armazenado em cache na memória privada.

A intenção desse modo é reduzir ainda mais a quantidade de memória privada usada pelo mecanismo de banco de dados do para armazenar em cache as

o cache de exibição só poderá ser usado se o uso do cache de arquivos de Windows estiver habilitado por meio da configuração de JET_paramEnableFileCache como **True**.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Falso</p> | 
| <p>Tipo:</p> | <p>Booliano</p> | 
| <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramLRUKCorrInterval*  
25  

Esse parâmetro define o intervalo de tempo em microssegundos sobre o qual dois acessos de página de banco de dados são considerados correlacionados. Esse intervalo de correlação controla a sensibilidade do algoritmo de substituição de página do cache (LRU-K) aos acessos de página sucessivos. Isso, por sua vez, afetará as páginas que ele escolhe manter em cache.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>128000</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 – 2147483647</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKHistoryMax*  
26  

Esse parâmetro define o número máximo de páginas de banco de dados não armazenadas em cache para as quais os tempos de acesso da página do banco de dados serão retidos. Esses registros de histórico permitem que o algoritmo de substituição de página do cache (LRU-K) detecte com mais precisão as páginas populares que foram removidas erroneamente do cache da página do banco de dados.

**Windows XP e Windows Server 2003:**  esse parâmetro é ignorado no Windows XP e no Windows Server 2003 e não afeta a operação do mecanismo de banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong> 1024</p><p><strong>Windows Vista:</strong> 100000</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 0 – 4194303</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKPolicy*  
27  

Esse parâmetro configura o número de acessos de página do banco de dados que são considerados para determinar a utilidade da página. Esse parâmetro é essencialmente o K no LRU-K, o algoritmo de substituição de página do cache de página do banco de dados.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>2</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>1-2</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKTimeout*  
28

Esse parâmetro indica o período de tempo em segundos após o qual uma página no cache de página do banco de dados é considerada como tendo perdido um acesso de página com a finalidade de considerar a utilidade da página.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>100</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 1 – 2147483647</p><p><strong>Windows Vista:</strong> 1 – 4294967295</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLRUKTrxCorrInterval*  
29  

Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.

*JET_paramStartFlushThreshold*  
31  

Esse parâmetro controla quando o cache de página do banco de dados começa a ressalir páginas do cache para dar espaço a páginas que não são armazenadas em cache. Quando o número de buffers de página no cache ficar abaixo desse limite, um processo em segundo plano será iniciado para reabastecer esse pool de buffers disponíveis. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido **por JET_paramCacheSizeMax**. Esse limite também deve ser sempre menor que o limite de parada conforme definido **por JET_paramStopFlushThreshold**.

A altura da distância do limite inicial determinará o tempo de resposta que o cache de página do banco de dados deve ter para produzir buffers disponíveis antes que o aplicativo precise deles. Um limite inicial alto dará ao processo em segundo plano mais tempo para reagir. No entanto, um limite inicial alto implica um limite de parada mais alto e reduzirá o tamanho efetivo do cache de página do banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 5 (1%)</p><p><strong>Windows Vista:</strong> 20000000 (1%)</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 – 1048575</p><p><strong>Windows XP:</strong> 1 – 4294967295</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | 
| <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramStopFlushThreshold*  
32  

Esse parâmetro controla quando o cache da página do banco de dados termina de ressalvar páginas do cache para dar espaço a páginas que não são armazenadas em cache. Quando o número de buffers de página no cache aumenta acima desse limite, o processo em segundo plano que foi iniciado para reabastecer esse pool de buffers disponíveis é interrompido. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido **por JET_paramCacheSizeMax**. Esse limite também deve ser sempre maior que o limite inicial, conforme definido **por JET_paramStartFlushThreshold**.

A distância entre o limite inicial e o limite de parada afeta a eficiência com a qual as páginas de banco de dados são liberados pelo processo em segundo plano. Uma lacuna maior fará com que seja mais provável que as gravações em páginas vizinhos possam ser combinadas. No entanto, um limite de parada alto reduzirá o tamanho efetivo do cache de página do banco de dados para páginas modificadas (Windows 2000) ou para todas as páginas (Windows XP e posterior).


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 10 (2%)</p><p><strong>Windows Vista:</strong> 40 milhões (2%)</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong> 1 a 1048575</p><p><strong>Windows XP:</strong> 1 a 4294967295</p><p><strong>Windows Vista:</strong>  Todos os valores</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Sim</p> | 
| <p>Afeta os recursos:</p> | <p>Sim</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
