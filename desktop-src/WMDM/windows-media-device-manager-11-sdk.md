---
title: Windows SDK do Media Gerenciador de Dispositivos 11
description: Windows SDK do Media Gerenciador de Dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Gerenciador de Dispositivos de mídia, sobre
- Gerenciador de Dispositivos, sobre
- MTP (protocolo de transferência de mídia)
- MTP (protocolo de transferência de mídia)
- classe de Armazenamento em massa (MSC)
- MSC (classe de Armazenamento em massa)
- Windows Gerenciador de Dispositivos de mídia, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- aplicativos de área de trabalho, sobre
- Windows Gerenciador de Dispositivos de mídia, provedores de serviço
- Gerenciador de Dispositivos, provedores de serviços
- provedores de serviço, sobre
- Windows Gerenciador de Dispositivos de mídia, plug-ins
- Gerenciador de Dispositivos, plug-Insp
- plug-ins, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e8b19b035f0210b7928dcc42c19d9519a63fe4eac3e5adaeded780c9d4c729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004806"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows SDK do Media Gerenciador de Dispositivos 11

> [!IMPORTANT]
> as APIs de Gerenciador de Dispositivos de mídia Windows agora estão incluídas no SDK do Windows. Nenhum download adicional do SDK é necessário.

 

o SDK (Software Development Kit) do Microsoft Windows Media Gerenciador de Dispositivos permite que você crie aplicativos e componentes de área de trabalho que podem se comunicar com dispositivos portáteis conectados. Windows A mídia Gerenciador de Dispositivos permite que seu aplicativo ou componente enumere, explore e troque arquivos com um dispositivo, consulte metadados e solicite informações de contagem de reprodução. aplicativos ou componentes criados em Windows mídia Gerenciador de Dispositivos têm uma API consistente para se comunicar com uma ampla gama de dispositivos, incluindo MTP (Media Transfer Protocol), MSC (massa Armazenamento Class), RAPI e outros dispositivos criados nas versões mais recentes e anteriores da tecnologia de mídia Windows.

você pode criar os seguintes itens usando o SDK do Windows Media Gerenciador de Dispositivos:

-   Aplicativos de área de trabalho, como players de mídia personalizados. toda a comunicação entre um aplicativo e um dispositivo portátil deve passar por Windows mídia Gerenciador de Dispositivos, que atua como um agente entre o aplicativo, o sistema Microsoft digital rights management e o provedor de serviços.
-   Provedores de serviços, que atuam como o link de comunicação entre um dispositivo personalizado e um aplicativo de área de trabalho. Embora a Microsoft forneça vários provedores de serviços que podem se comunicar com a maioria dos dispositivos prontos para uso, você pode criar um provedor de serviços personalizado para personalizar a comunicação entre um dispositivo e um aplicativo de área de trabalho.
-   Plug-ins, que podem executar tarefas como solicitar e registrar contas de reprodução em dispositivos. esses plug-ins podem ser anexados a outros aplicativos de área de trabalho, como o Windows Media Player para enviar informações aos provedores de conteúdo para lidar com pagamentos de royalties para artistas.

para baixar o SDK do Windows media Gerenciador de Dispositivos, consulte [a página de download do Windows media](https://msdn.microsoft.com/windows/desktop/aa904949) no site do MSDN.

este SDK é um componente do Microsoft Windows Media Software Development Kit. outros componentes incluem o sdk do formato de mídia Windows, o sdk do Windows Media Services, o sdk do codificador de mídia do Windows, o sdk do Windows media rights Manager e o sdk do Windows Media Player.

Esta documentação inclui as seções a seguir.



| Seção                                            | Descrição                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução](getting-started.md)             | descreve o que há de novo nesta versão do Windows media Gerenciador de Dispositivos, fornece uma visão geral de como Windows mídia Gerenciador de Dispositivos funciona, descreve o que será necessário para desenvolver um aplicativo ou provedor de serviços e explica os exemplos fornecidos com o SDK. |
| [Guia de programação](programming-guide.md)         | Discute como criar aplicativos e provedores de serviços.                                                                                                                                                                                                      |
| [Referência de programação](programming-reference.md) | fornece informações de referência do C++ para as interfaces, métodos, classes e estruturas com suporte no SDK do Windows Media Gerenciador de Dispositivos.                                                                                                                      |
| [*Glossário*](wmdm-glossary.md)                    | Define os termos usados nesta documentação.                                                                                                                                                                                                                       |



 

 

 




