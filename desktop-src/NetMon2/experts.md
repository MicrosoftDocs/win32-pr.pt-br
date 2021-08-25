---
description: Um especialista é uma DLL (biblioteca de vínculo dinâmico) do Microsoft Win32 que analisa o tráfego de rede coletado por um NPP (provedor de pacotes de rede) e colocado em um arquivo de captura.
ms.assetid: 57d8164e-f587-4bb9-a0b1-6094037e584c
title: Especialista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f4c3e34a9f6b8b36fdc6aa4793acfa5b652b9fa2c2117afc62943c0947af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890907"
---
# <a name="expert"></a>Especialista

Um especialista é uma DLL (biblioteca de vínculo dinâmico) do Microsoft Win32 que analisa o tráfego de rede coletado por um NPP ( [*provedor de pacotes de rede*](n.md) ) e colocado em um arquivo de captura. Depois que os dados são capturados e armazenados em um arquivo de captura, o especialista trabalha com um analisador, também conhecido como analisador de protocolo, para analisar os dados no arquivo. Por exemplo, você pode examinar os quadros do arquivo de captura e usar um [*analisador*](p.md) para reconhecer protocolos como o protocolo SMB ou TCP/IP (Transmission Control Protocol/Internet Protocol).

Você pode criar um especialista para trabalhar com todos os analisadores de Monitor de Rede e quaisquer analisadores que você criar por conta própria.

Depois que uma correspondência solicitada de protocolos identifica um quadro específico, o especialista extrai dados do quadro. Você pode programar o especialista para manipular informações em dados utilizáveis que o Monitor de Rede Visualizador de Eventos exibe.

Você pode configurar um especialista em tempo de execução e, em seguida, usar Monitor de Rede para salvar os dados de configuração do usuário para reutilização com arquivos de captura diferentes. Você pode usar um especialista para fornecer dados de correlação e resoluções personalizadas para usuários finais. Para obter mais informações sobre a criação de informações de configuração baseadas em HTML, consulte [página de referência de evento](event-reference-page.md).

Durante a instalação do Monitor de Rede, as seguintes DLLs de especialistas são instaladas no subdiretório especialistas:

-   Coalesce.dll
-   Propdist.dll
-   Protdist.dll
-   Resptime.dll
-   Tcpipe.dll
-   Topuser.dll

Quando você inicia Monitor de Rede, a função [**DllMain**](dllmain-expert.md) cria todos os especialistas no subdiretório especialistas. Quando o usuário seleciona **especialistas** no menu **ferramentas** da interface do usuário do monitor de rede, monitor de rede carrega as DLLs de especialistas. O especialista é chamado por meio do ponto de entrada do [especialista de registro](register-expert.md) para fornecer detalhes básicos sobre o especialista.

![caixa de diálogo especialistas no monitor de rede](images/expick.png)

Monitor de Rede chama as seguintes funções para gerenciar o especialista:

-   [**DllMain**](dllmain-expert.md)
-   [**Registrar especialista**](register-expert.md)
-   [**Executar**](run.md)
-   [**Configurar**](configure.md)

O especialista deve implementar cada uma das funções anteriores.

 

 



