---
description: Interface de programação de aplicativo WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interface de programação de aplicativo WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791310"
---
# <a name="wpd-application-programming-interface"></a>Interface de programação de aplicativo WPD

Aplicativos criados em dispositivos portáteis do Windows podem explorar um dispositivo, enviar e receber conteúdo e até mesmo controlar o dispositivo, por exemplo, tirar uma foto ou enviar uma mensagem de texto. O sistema foi projetado para ser flexível, de modo que muitos tipos de dispositivos possam ser explorados e extensíveis para que os desenvolvedores de driver possam definir propriedades e comandos personalizados para dispositivos personalizados.

A tabela a seguir descreve os principais tópicos desta documentação.



| Tópico                                                                                                                  | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Requisitos gerais para o desenvolvimento de aplicativos](general-requirements-for-application-development.md)               | Requisitos de hardware e software para desenvolver drivers e aplicativos usando dispositivos portáteis do Windows.     |
| [Requisitos para aplicativos do Windows Media DRM-Enabled](requirements-for-windows-media-drm-enabled-applications.md) | Propriedades que são necessárias para habilitar transferências de conteúdo protegidas por DRM do Windows Media.                      |
| [Amostras](sample.md)                                                                                                  | Descrição de dois aplicativos de área de trabalho de linha de comando que são fornecidos com essa Software Development Kit. |
| [Visão geral do aplicativo](application-overview.md)                                                                       | Conceitos principais usados em dispositivos portáteis do Windows.                                                             |
| [Guia de programação](programming-guide.md)                                                                             | As principais tarefas que um aplicativo executará com instruções passo a passo e trechos de código.              |
| [Referência de programação](programming-reference.md)                                                                     | Guia de referência para as interfaces e os tipos de dados definidos por dispositivos portáteis do Windows.                      |



 

Aplicativos criados no Windows Media Gerenciador de Dispositivos ou aquisição de imagem do Windows podem acessar dispositivos portáteis do Windows por meio de uma camada de compatibilidade.

A Microsoft fornece vários drivers para protocolos e dispositivos padrão, incluindo dispositivos MTP (protocolo de transporte de mídia) e dispositivos MSC (classe de armazenamento em massa). Se você estiver familiarizado com a estrutura de driver User-Mode, poderá desenvolver seus próprios drivers para dispositivos personalizados.

 

 



