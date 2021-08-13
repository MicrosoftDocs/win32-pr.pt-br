---
description: 'Saiba mais sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bd72ecab62eeccb3ed7e586e2e793bdb9796f09a57686e70d9177eb496316760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254318"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_errcat"></a>JET_ERRCAT

O **JET_ERRCAT** de constantes descreve classificações de nível superior ou categorias de erros. Esse grupo de constantes permite que os aplicativos definam o tratamento padrão para uma classificação de erros, em vez de tratar cada caso de erro individualmente. Ele também garante que o aplicativo não precisa lidar com novas condições de erro incluídas em classificações existentes.

Observação: esta documentação baseia-se em uma versão preliminar do Mecanismo Armazenamento Extensível. Essas informações estão sujeitas a alterações.

As **JET_ERRCAT** constantes são organizadas em uma hierarquia específica de condições e subcondições, da seguinte forma:

|--- operação de |---(al) | |--- | |--- recurso de | |--- de E/S fatal | |--- memória | |--- | |--- cota de | |--- de disco | |--- dados | |--- corrupção | |--- fragmentação de | |--- | |--- |--- estado de | |--- |--- de api de |---

A tabela a seguir lista as **JET_ERRCAT** constantes e fornece uma descrição e informações de recuperação, conforme aplicável.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valor</p></th>
<th><p>Descrição</p></th>
<th><p>Recuperação</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>Uma categoria de erro inválida.</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>A categoria de nível superior (nenhum erro deve ser dessa classe).</p></td>
<td><p>Consulte as constantes de erro específicas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>Representa erros que podem ocorrer a qualquer momento devido a condições não controláveis e geralmente são temporários. Consulte subcategorias, se especificado.</p></td>
<td><p>Tentar novamente e, se o erro continuar, informe o operador.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>Representa erros fatais que, quando ocorrem, criam um risco de que o ESE não possa continuar de maneira segura (geralmente transacional) e os dados possam ficar corrompidos.</p></td>
<td><p>Reinicie a instância ou o processo. Se o problema persistir, informe o operador .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>Representa erros de E/S, que vêm do sistema operacional e estão fora do controle do ESE. Esse tipo de erro pode ser temporário.</p></td>
<td><p>Tentar novamente e, se o erro continuar, peça ao operador para verificar o disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>Representa uma categoria de erros relacionados à falta de condições de recurso.</p></td>
<td><p>Consulte subcategorias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>Representa um erro causado pela falta de memória.</p></td>
<td><p>Tentar novamente após um período de tempo, liberar memória ou encerrar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>Determinados recursos de especialização estão em pools de um determinado tamanho, facilitando a &quot; &quot; detecção de vazamentos desses recursos.</p></td>
<td><p>O aplicativo deve <strong>Assert()</strong> para detectar esses problemas durante o desenvolvimento. No entanto, no código de varejo, o aplicativo deve tratar isso como um erro de memória.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>Representa um erro causado pela falta de espaço em disco.</p></td>
<td><p>Tentar novamente mais tarde para determinar se há mais espaço em disco disponível ou pedir ao operador para liberar algum espaço em disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>Representa uma categoria de nível superior para erros relacionados a dados.</p></td>
<td><p>Consulte subcategorias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>Representa um problema de corrupção, que geralmente é permanente sem ação corretiva.</p></td>
<td><p>Restaure do backup usando a operação de reparo de utilitários ESE (essa operação restaura apenas os dados que são deixados/com perda). Além disso, quando o método recovery(JetInit) é usado, a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, <a href="gg269296(v=exchg.10).md">consulte JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>Representa um erro no qual o banco de dados e/ou arquivos de log estão em um estado inconsistente e não podem ser reconciliados. Esse erro pode ser causado por incompatibilidade de aplicativo/administrador.</p></td>
<td><p>Restaure do backup usando a operação de reparo de utilitários ESE (que restaura apenas os dados que são deixados/com perda). Além disso, no caso da operação <strong>de recuperação (JetInit),</strong> a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, <a href="gg269296(v=exchg.10).md">consulte JET_bitReplayIgnoreLostLogs</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>Representa uma classe de erros em que alguns recursos internos persistentes se esgotaram.</p></td>
<td><p>Para erros de banco de dados, a desfragmentação offline corrigirá o problema. Para os arquivos de log, primeiro recupere todos os bancos de dados anexados para um desligamento limpo e, em seguida, exclua todos os arquivos de log e o ponto de verificação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>Consulte subcategorias.</p></td>
<td><p>Consulte subcategorias.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>Representa um erro de uso. O código do cliente não passou os argumentos corretos para a API <strong>jet.</strong> Esse erro persistirá com a tentativa de novamente.</p></td>
<td><p>O código do cliente deve usar <strong>o método Assert()</strong> para garantir que essa classe de erros não seja retornada, de modo que os problemas possam ser capturados durante o desenvolvimento. No varejo, o aplicativo deve notificar o operador sobre o erro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>Representa uma classe de mensagens que a API pode retornar para descrever o estado do banco de dados. Por exemplo, o <a href="gg294103(v=exchg.10).md">método JetSeek()</a> pode retornar <strong>JET_errRecordNotFound</strong> quando o registro solicitado não foi encontrado.</p></td>
<td><p>Varia de acordo com a API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>Representa erros que são de uma versão anterior do mecanismo. Esses erros não devem ser retornados pelo mecanismo atual.</p></td>
<td><p>Desconhecido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>Uma constante que indica o final da enumeração.</p></td>
<td><p>N/D</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>

