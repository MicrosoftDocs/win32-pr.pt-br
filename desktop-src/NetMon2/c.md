---
description: Glossário de Monitor de Rede termos que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749773"
---
# <a name="c-network-monitor"></a>C (Monitor de Rede)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**captura**
</dt> <dd>

Dados de tráfego de rede que são coletados em quadros. Um NPP (provedor de pacotes de rede) executa uma captura. Consulte também [*captura atrasada*](d.md)e *captura em tempo real*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**arquivo de captura**
</dt> <dd>

Um arquivo que Monitor de Rede cria para armazenar dados capturados. A extensão de nome de arquivo. Cap identifica um arquivo de captura. Monitor de Rede gera aleatoriamente um nome de arquivo de captura, mas você pode alterar o nome do arquivo ao salvar o arquivo de captura.

Monitor de Rede cria um arquivo de captura cada vez que o processo de captura é iniciado e mantém o arquivo aberto durante o processo de captura. Você não pode acessar o conteúdo de um arquivo de captura até que o processo de captura seja interrompido e o arquivo de captura seja fechado.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro de captura**
</dt> <dd>

Um conjunto de funções Monitor de Rede usadas para restringir os quadros de entrada que um aplicativo NPP (provedor de pacotes de rede) usa.

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**gatilho de captura**
</dt> <dd>

Um evento de gatilho que é definido para interromper o processo de captura. O evento de gatilho de captura pode ser um arquivo de captura temporário que é direcionado para um nível específico ou padrão de dados que ocorre em um quadro capturado.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**dados capturados**
</dt> <dd>

Quadros que têm um conjunto definido de critérios. Os quadros de dados estão contidos em um arquivo de captura temporário.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Estatísticas de conversa**
</dt> <dd>

Estatísticas do tráfego de rede salvo durante uma captura. Essas estatísticas incluem informações de estação e de sessão que começam quando o processo de captura é iniciado e terminam quando a captura é interrompida. Se você pausar o processo de captura, Monitor de Rede continuará a adicionar estatísticas quando você retomar o processo. Para recuperar estatísticas de conversa, chame o método **GetConversationStatistics** para a interface que você está usando.

</dd> </dl>

 

 



