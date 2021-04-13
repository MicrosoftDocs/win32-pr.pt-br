---
title: SDK do Windows Media Gerenciador de Dispositivos 11
description: SDK do Windows Media Gerenciador de Dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Gerenciador de Dispositivos, sobre
- Gerenciador de Dispositivos, sobre
- MTP (protocolo de transferência de mídia)
- MTP (protocolo de transferência de mídia)
- Classe de armazenamento em massa (MSC)
- MSC (classe de armazenamento em massa)
- Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- aplicativos de área de trabalho, sobre
- Windows Media Gerenciador de Dispositivos, provedores de serviços
- Gerenciador de Dispositivos, provedores de serviços
- provedores de serviço, sobre
- Gerenciador de Dispositivos de mídia do Windows, plug-ins
- Gerenciador de Dispositivos, plug-Insp
- plug-ins, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366844"
---
# <a name="windows-media-device-manager-11-sdk"></a>SDK do Windows Media Gerenciador de Dispositivos 11

> [!IMPORTANT]
> As APIs do Windows Media Gerenciador de Dispositivos agora estão incluídas no SDK do Windows. Nenhum download adicional do SDK é necessário.

 

O SDK (Software Development Kit) do Microsoft Windows Media Gerenciador de Dispositivos permite que você crie aplicativos e componentes de área de trabalho que podem se comunicar com dispositivos portáteis conectados. O Windows Media Gerenciador de Dispositivos permite que seu aplicativo ou componente enumere, explore e troque arquivos com um dispositivo, consulte metadados e solicite informações de contagem de reprodução. Aplicativos ou componentes criados no Windows Media Gerenciador de Dispositivos têm uma API consistente para se comunicar com uma ampla gama de dispositivos, incluindo o MTP (Media Transfer Protocol), o MSC (classe de armazenamento em massa), o RAPI e outros dispositivos criados nas versões mais recentes e anteriores da tecnologia Windows Media.

Você pode criar os seguintes itens usando o SDK do Windows Media Gerenciador de Dispositivos:

-   Aplicativos de área de trabalho, como players de mídia personalizados. Toda a comunicação entre um aplicativo e um dispositivo portátil deve passar pelo Windows Media Gerenciador de Dispositivos, que atua como um agente entre o aplicativo, o sistema Microsoft Digital Rights Management e o provedor de serviços.
-   Provedores de serviços, que atuam como o link de comunicação entre um dispositivo personalizado e um aplicativo de área de trabalho. Embora a Microsoft forneça vários provedores de serviços que podem se comunicar com a maioria dos dispositivos prontos para uso, você pode criar um provedor de serviços personalizado para personalizar a comunicação entre um dispositivo e um aplicativo de área de trabalho.
-   Plug-ins, que podem executar tarefas como solicitar e registrar contas de reprodução em dispositivos. Esses plug-ins podem ser anexados a outros aplicativos de área de trabalho, como o Windows Media Player, para enviar informações aos provedores de conteúdo para lidar com pagamentos de royalties para artistas.

Para baixar o SDK do Windows Media Gerenciador de Dispositivos, consulte [a página de download do Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) no site do MSDN.

Este SDK é um componente do Microsoft Windows Media Software Development Kit. Outros componentes incluem o SDK do Windows Media Format, o SDK do Windows Media Services, o Windows Media Encoder SDK, o SDK do Windows Media Rights Manager e o SDK do Windows Media Player.

Esta documentação inclui as seções a seguir.



| Seção                                            | Descrição                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução](getting-started.md)             | Descreve o que há de novo nesta versão do Windows Media Gerenciador de Dispositivos, fornece uma visão geral de como funciona o Windows Media Gerenciador de Dispositivos, descreve o que será necessário para desenvolver um aplicativo ou provedor de serviços e explica os exemplos fornecidos com o SDK. |
| [Guia de programação](programming-guide.md)         | Discute como criar aplicativos e provedores de serviços.                                                                                                                                                                                                      |
| [Referência de programação](programming-reference.md) | Fornece informações de referência de C++ para as interfaces, métodos, classes e estruturas com suporte no SDK do Windows Media Gerenciador de Dispositivos.                                                                                                                      |
| [*Glossário*](wmdm-glossary.md)                    | Define os termos usados nesta documentação.                                                                                                                                                                                                                       |



 

 

 




