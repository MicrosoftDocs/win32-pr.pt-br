---
description: 'Saiba mais sobre: propriedades do SystemParameters'
title: Propriedades do SystemParameters
TOCTitle: SystemParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55104035
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 13b2735f699fe2943dcb63bf262c8c708e61df754ed6799f2fb948119755d2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890674"
---
# <a name="systemparameters-properties"></a>Propriedades do SystemParameters

Incluir membros protegidos  
Incluir membros herdados  

O tipo [SystemParameters](./systemparameters-class.md) expõe os membros a seguir.

## <a name="properties"></a>Propriedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>Obtém o tamanho máximo de um indicador. <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Obtém ou define o tamanho do cache de banco de dados em páginas. Por padrão, o cache do banco de dados ajustará automaticamente seu tamanho, a definição dessa propriedade com um valor diferente de zero fará com que o cache se ajuste ao tamanho do destino.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Obtém ou define o tamanho máximo do cache de página do banco de dados. O tamanho está em páginas de banco de dados. Se esse parâmetro for deixado para seu valor padrão, o tamanho máximo do cache será definido como o tamanho da memória física quando JetInit for chamado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Obtém ou define o tamanho mínimo do cache de página de banco de dados, em páginas de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Obtém o número máximo de componentes em uma chave de classificação ou de índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuration</a></td>
<td>Obtém ou define um valor que especifica os valores padrão para o conjunto inteiro de parâmetros do sistema. Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração. Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão. Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória. Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais. com suporte no Windows Vista e em cima. ignorado no Windows XP e no Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Obtém ou define o tamanho das páginas do banco de dados, em bytes.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>Obtém ou define um valor que indica se o mecanismo de banco de dados aceita ou rejeita alterações em um subconjunto dos parâmetros do sistema. Esse parâmetro é usado em conjunto com a <a href="dn351218(v=exchg.10).md">configuração</a> para impedir que alguns parâmetros do sistema sejam definidos fora dos padrões da configuração selecionada. com suporte no Windows Vista e em cima. ignorado no Windows XP e no Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Obtém ou define um valor que indica se o mecanismo de banco de dados deve usar o cache de arquivos do so para todos os arquivos gerenciados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Obtém ou define um valor que indica se o mecanismo de banco de dados deve usar a e/s de arquivo mapeada de memória para arquivos de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Obtém ou define o nível de detalhe das mensagens de log de eventos emitidas para o log de eventos pelo mecanismo de banco de dados. Números mais altos resultarão em mensagens de log de eventos mais detalhadas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">Exceçãoaction</a></td>
<td>Obtém ou define o valor que codifica o que fazer com exceções geradas no JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>Obtém ou define o conjunto de ações a serem executadas no IOs que aparecem travadas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Obtém ou define o limite para o que é considerado uma e/s suspensa que deve ser tratada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">Mais</a></td>
<td>Obtém o tamanho máximo da chave. Isso depende da versão do ESENT e do tamanho da página do banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Obtém ou define a compatibilidade com versões anteriores do mecanismo de banco de dados com as convenções de nomenclatura de arquivo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Obtém o tamanho dos blocos LV. Isso depende do tamanho da página do banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Obtém ou define o número máximo de instâncias que podem ser criadas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Obtém ou define a menor quantidade de dados que devem ser compactados com a compactação do Xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Esse parâmetro controla quantas e/SS de arquivo de banco de dados podem ser enfileiradas por disco no sistema operacional do host ao mesmo tempo. Um valor maior para esse parâmetro pode ajudar significativamente o desempenho de um aplicativo de banco de dados grande.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Obtém ou define o nome amigável para esta instância do processo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Obtém ou define o limite no qual o cache da página do banco de dados começa a remover páginas do cache para liberar espaço para páginas que não estão armazenadas em cache. Quando o número de buffers de página no cache cair abaixo desse limite, um processo em segundo plano será iniciado para reabastecer o pool de buffers disponíveis. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax. Esse limite também deve ser menor que o limite de parada definido por JET_paramStopFlushThreshold. A altura da distância do limite inicial determinará o tempo de resposta que o cache da página do banco de dados deve ter para produzir os buffers disponíveis antes que o aplicativo precise deles. Um limite de início alto dará ao processo em segundo plano mais tempo para reagir. No entanto, um limite de início alto implica um limite de parada maior e reduzirá o tamanho efetivo do cache de página do banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriedade pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Obtém ou define o limite no qual o cache da página do banco de dados encerra a remoção de páginas do cache para liberar espaço para páginas que não são armazenadas em cache. Quando o número de buffers de página no cache ultrapassar esse limite, o processo em segundo plano que foi iniciado para reabastecer o pool de buffers disponíveis será interrompido. Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax. Esse limite também deve ser maior que o limite de início definido por JET_paramStartFlushThreshold. A distância entre o limite inicial e o limite de interrupção afeta a eficiência com a qual as páginas de banco de dados são liberadas pelo processo em segundo plano. Um intervalo maior fará com que seja mais provável que as gravações nas páginas vizinhas possam ser combinadas. No entanto, um limite de interrupção alto reduzirá o tamanho efetivo do cache de página do banco de dados.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe SystemParameters](./systemparameters-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
