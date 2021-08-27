---
description: 'Saiba mais sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 951c26d0b1576d565b90f3bceeef9eb835e4be45
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476842"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_errcat"></a>JET_ERRCAT

O **JET_ERRCAT** grupo de constantes descreve as classificações de nível superior ou as categorias de erros. Esse grupo de constantes permite que os aplicativos definam o tratamento padrão para uma classificação de erros, em vez de manipular cada caso de erro individualmente. Ele também garante que o aplicativo não precise lidar com novas condições de erro incluídas nas classificações existentes.

observação: esta documentação se baseia em uma versão preliminar do mecanismo de Armazenamento extensível. Essas informações estão sujeitas a alterações.

As constantes **JET_ERRCAT** são organizadas em uma hierarquia específica de condições e subcondiçãos, da seguinte maneira:

| Erro de---|---operação (al) | |---fatal | |---IO | |---recurso | |---memória | |---cota | |---disco | |---dados | |---corrupção | |---de estado inconsistente | |---fragmentação | |---

A tabela a seguir lista as constantes **JET_ERRCAT** e fornece uma descrição e informações de recuperação, conforme aplicável.


| <p>Constante/valor</p> | <p>Descrição</p> | <p>Recuperação</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Uma categoria de erro inválida.</p> | <p>N/D</p> | 
| <p>JET_errcatError 1</p> | <p>A categoria de nível superior (nenhum erro deve ser dessa classe).</p> | <p>Consulte as constantes de erro específicas.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Representa os erros que podem ocorrer a qualquer momento devido a condições não controláveis e geralmente são temporários. Consulte subcategorias, se especificado.</p> | <p>Tente novamente e, se o erro continuar, informe o operador.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Representa erros fatais que, quando ocorrem, criam um risco de que o ESE não possa continuar em uma maneira segura (geralmente transacional) e os dados possam ser corrompidos.</p> | <p>Reinicie a instância ou o processo. Se o problema persistir, informe o operador.</p> | 
| <p>JET_errcatIO 4</p> | <p>Representa os erros de e/s, que vêm do sistema operacional e estão fora do controle do ESE. Esse tipo de erro pode ser temporário.</p> | <p>Tente novamente e, se o erro continuar, peça ao operador para verificar o disco.</p> | 
| <p>JET_errcatResource 5</p> | <p>Representa uma categoria de erros relacionados à falta de condições de recurso.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Representa um erro causado por falta de memória.</p> | <p>Tente novamente após um período de tempo, libere memória ou saia.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Determinados recursos de "especialidade" estão em pools de um determinado tamanho, facilitando a detecção de vazamentos desses recursos.</p> | <p>O aplicativo deve <strong>declarar ()</strong> para detectar esses problemas durante o desenvolvimento. No entanto, no código de varejo, o aplicativo deve tratá-lo como um erro de memória.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Representa um erro causado por falta de espaço em disco.</p> | <p>Tente novamente mais tarde para determinar se há mais espaço em disco disponível ou peça ao operador para liberar espaço em disco.</p> | 
| <p>JET_errcatData 9</p> | <p>Representa uma categoria de nível superior para erros relacionados a dados.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Representa um problema de corrupção, que geralmente é permanente sem ação corretiva.</p> | <p>Restaure a partir do backup usando a operação de reparo de utilitários ESE (essa operação restaura somente os dados que são restantes/com perda). Além disso, quando o método Recovery (JetInit) é usado, a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, consulte <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Representa um erro no qual os arquivos de banco de dados e/ou de log estão em um estado inconsistente e não podem ser reconciliados. Esse erro pode ser causado por um aplicativo/administrador indisponível.</p> | <p>Restaure a partir do backup usando a operação de reparo de utilitários ESE (que restaura apenas os dados que são restantes/com perda). Também no caso da operação de <strong>recuperação (JetInit)</strong> , a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, consulte <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Representa uma classe de erros em que um recurso interno persistente foi executado.</p> | <p>Para erros de banco de dados, a desfragmentação offline corrigirá o problema. Para os arquivos de log, primeiro Recupere todos os bancos de dados anexados para um desligamento normal e, em seguida, exclua todos os arquivos de log e o ponto de verificação.</p> | 
| <p>JET_errcatApi 13</p> | <p>Consulte subcategorias.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Representa um erro de uso. O código do cliente não passou os argumentos corretos para a API do <strong>Jet</strong> . Esse erro persistirá com a repetição.</p> | <p>O código do cliente deve usar o método <strong>Assert ()</strong> para garantir que essa classe de erros não seja retornada, de modo que os problemas possam ser detectados durante o desenvolvimento. No varejo, o aplicativo deve notificar o operador sobre o erro.</p> | 
| <p>JET_errcatState 15</p> | <p>Representa uma classe de mensagens que a API pode retornar para descrever o estado do banco de dados. Por exemplo, o método <a href="gg294103(v=exchg.10).md">JetSeek ()</a> pode retornar <strong>JET_errRecordNotFound</strong> quando o registro solicitado não foi encontrado.</p> | <p>Varia de acordo com a API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Representa os erros que são de uma versão anterior do mecanismo. Esses erros não devem ser retornados pelo mecanismo atual.</p> | <p>Desconhecido.</p> | 
| <p>JET_errcatMax 17</p> | <p>Uma constante que indica o final da enumeração.</p> | <p>N/D</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>requer Windows 8 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


