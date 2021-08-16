---
description: Glossário de Monitor de Rede termos que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31993c18307ab1beaa1b6cff379626b9398987d6ad9475947c4aeb4d09dd32e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367432"
---
# <a name="c-network-monitor"></a>C (Monitor de Rede)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**Capturar**
</dt> <dd>

Dados de tráfego de rede coletados em quadros. Um provedor de pacotes de rede (NPP) executa uma captura. Confira também [*captura atrasada*](d.md)e captura em *tempo real*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capturar arquivo**
</dt> <dd>

Um arquivo que Monitor de Rede para armazenar dados capturados. A extensão de nome de arquivo .cap identifica um arquivo de captura. Monitor de Rede gera aleatoriamente um nome de arquivo de captura, mas você pode alterar o nome do arquivo ao salvar o arquivo de captura.

Monitor de Rede cria um arquivo de captura sempre que o processo de captura é iniciado e, em seguida, mantém o arquivo aberto durante o processo de captura. Você não pode acessar o conteúdo de um arquivo de captura até que o processo de captura seja interrompido e o arquivo de captura seja fechado.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro de captura**
</dt> <dd>

Um conjunto de Monitor de Rede usadas para restringir quadros de entrada que um aplicativo NPP (provedor de pacotes de rede) usa.

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**gatilho de captura**
</dt> <dd>

Um evento de gatilho definido para interromper o processo de captura. O evento de gatilho de captura pode ser um arquivo de captura temporário direcionado para um nível específico ou um padrão de dados que ocorre em um quadro capturado.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**dados capturados**
</dt> <dd>

Quadros que têm um conjunto definido de critérios. Os quadros de dados estão contidos em um arquivo de captura temporário.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**estatísticas de conversa**
</dt> <dd>

Estatísticas de tráfego de rede salvas durante uma captura. Essas estatísticas incluem informações de estação e sessão que começam quando o processo de captura é iniciado e terminam quando a captura é interrompida. Se você pausar o processo de captura, Monitor de Rede continuará adicionando estatísticas ao retomar o processo. Para recuperar estatísticas de conversa, chame o **método GetConversationStatistics** para a interface que você está usando.

</dd> </dl>

 

 



