---
description: 'Saiba mais sobre: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: dee8dc7850cf69957c360253b942117739fe405b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987549"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_errcat"></a>JET_ERRCAT

O **JET_ERRCAT** grupo de constantes descreve classificações ou categorias de erros de nível superior. Esse grupo de constantes permite que os aplicativos definam o tratamento padrão para uma classificação de erros, em vez de tratar cada caso de erro individualmente. Ele também garante que o aplicativo não precisa lidar com novas condições de erro incluídas em classificações existentes.

Observação: esta documentação baseia-se em uma versão preliminar do Mecanismo Armazenamento Extensível. Essas informações estão sujeitas a alterações.

As **JET_ERRCAT** constantes são organizadas em uma hierarquia específica de condições e subcondições, da seguinte forma:

|--- Operação de |---(al) | |--- recurso | |--- de | |--- de E/S fatal | |--- memória | |--- cota de | |--- disco | |--- dados | |--- corrupção | |--- fragmentação de | |--- | |--- estado de |--- de | |--- |--- de | |---

A tabela a seguir lista as **JET_ERRCAT** constantes e fornece uma descrição e informações de recuperação, conforme aplicável.


| <p>Constante/valor</p> | <p>Descrição</p> | <p>Recuperação</p> | 
|-----------------------|--------------------|-----------------|
| <p>JET_errcatUnknown 0</p> | <p>Uma categoria de erro inválida.</p> | <p>N/D</p> | 
| <p>JET_errcatError 1</p> | <p>A categoria de nível superior (nenhum erro deve ser dessa classe).</p> | <p>Confira as constantes de erro específicas.</p> | 
| <p>JET_errcatOperation 2</p> | <p>Representa erros que podem ocorrer a qualquer momento devido a condições não controláveis e geralmente são temporários. Consulte subcategorias, se especificado.</p> | <p>Tentar novamente e, se o erro continuar, informe o operador.</p> | 
| <p>JET_errcatFatal 3</p> | <p>Representa erros fatais que, quando ocorrem, criam um risco de que o ESE não possa continuar de maneira segura (geralmente transacional) e os dados possam ficar corrompidos.</p> | <p>Reinicie a instância ou o processo. Se o problema persistir, informe o operador .</p> | 
| <p>JET_errcatIO 4</p> | <p>Representa erros de E/S, que vêm do sistema operacional e estão fora do controle do ESE. Esse tipo de erro pode ser temporário.</p> | <p>Tentar novamente e, se o erro continuar, peça ao operador para verificar o disco.</p> | 
| <p>JET_errcatResource 5</p> | <p>Representa uma categoria de erros relacionados à falta de condições de recurso.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatMemory 6</p> | <p>Representa um erro causado pela falta de memória.</p> | <p>Tentar novamente após um período de tempo, liberar memória ou encerrar.</p> | 
| <p>JET_errcatQuota 7</p> | <p>Determinados recursos de "especialização" estão em pools de um determinado tamanho, facilitando a detecção de vazamentos desses recursos.</p> | <p>O aplicativo deve <strong>Assert()</strong> para detectar esses problemas durante o desenvolvimento. No entanto, no código de varejo, o aplicativo deve tratar isso como um erro de memória.</p> | 
| <p>JET_errcatDisk 8</p> | <p>Representa um erro causado pela falta de espaço em disco.</p> | <p>Tentar novamente mais tarde para determinar se há mais espaço em disco disponível ou pedir ao operador para liberar algum espaço em disco.</p> | 
| <p>JET_errcatData 9</p> | <p>Representa uma categoria de nível superior para erros relacionados a dados.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatCorruption 10</p> | <p>Representa um problema de corrupção, que geralmente é permanente sem ação corretiva.</p> | <p>Restaure do backup usando a operação de reparo de utilitários ESE (essa operação restaura apenas os dados que são deixados/com perda). Além disso, quando o método recovery(JetInit) é usado, a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, <a href="gg269296(v=exchg.10).md">consulte JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatInconsistent 11</p> | <p>Representa um erro no qual o banco de dados e/ou arquivos de log estão em um estado inconsistente e não podem ser reconciliados. Esse erro pode ser causado por incompatibilidade de aplicativo/administrador.</p> | <p>Restaure do backup usando a operação de reparo de utilitários ESE (que restaura apenas os dados que são deixados/com perda). Além disso, no caso da operação <strong>de recuperação (JetInit),</strong> a recuperação pode ser executada permitindo a perda de dados (para obter mais informações, <a href="gg269296(v=exchg.10).md">consulte JET_bitReplayIgnoreLostLogs</a>.</p> | 
| <p>JET_errcatFragmentation 12</p> | <p>Representa uma classe de erros em que alguns recursos internos persistentes se esgotaram.</p> | <p>Para erros de banco de dados, a desfragmentação offline corrigirá o problema. Para os arquivos de log, primeiro recupere todos os bancos de dados anexados para um desligamento limpo e, em seguida, exclua todos os arquivos de log e o ponto de verificação.</p> | 
| <p>JET_errcatApi 13</p> | <p>Consulte subcategorias.</p> | <p>Consulte subcategorias.</p> | 
| <p>JET_errcatUsage 14</p> | <p>Representa um erro de uso. O código do cliente não passou os argumentos corretos para a API <strong>jet.</strong> Esse erro persistirá com a tentativa de novamente.</p> | <p>O código do cliente deve usar <strong>o método Assert()</strong> para garantir que essa classe de erros não seja retornada, de modo que os problemas possam ser capturados durante o desenvolvimento. No varejo, o aplicativo deve notificar o operador sobre o erro.</p> | 
| <p>JET_errcatState 15</p> | <p>Representa uma classe de mensagens que a API pode retornar para descrever o estado do banco de dados. Por exemplo, o <a href="gg294103(v=exchg.10).md">método JetSeek()</a> pode retornar <strong>JET_errRecordNotFound</strong> quando o registro solicitado não foi encontrado.</p> | <p>Varia de acordo com a API.</p> | 
| <p>JET_errcatObsolete 16</p> | <p>Representa erros que são de uma versão anterior do mecanismo. Esses erros não devem ser retornados pelo mecanismo atual.</p> | <p>Desconhecido.</p> | 
| <p>JET_errcatMax 17</p> | <p>Uma constante que indica o final da enumeração.</p> | <p>N/D</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows 8 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 


