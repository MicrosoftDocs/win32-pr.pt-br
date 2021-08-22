---
description: Interface de programação de aplicativo WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interface de programação de aplicativo WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5937cf14e7679bb9d9ca487b12ec546fb1751e3c94930f83c4aed3be5ed71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083360"
---
# <a name="wpd-application-programming-interface"></a>Interface de programação de aplicativo WPD

Os aplicativos Windows dispositivos portáteis podem explorar um dispositivo, enviar e receber conteúdo e até mesmo controlar o dispositivo, por exemplo, tirar uma foto ou enviar uma mensagem de texto. O sistema foi projetado para ser flexível para que muitos tipos de dispositivos possam ser explorados e extensíveis para que os desenvolvedores de driver possam definir propriedades e comandos personalizados para dispositivos personalizados.

A tabela a seguir descreve os principais tópicos desta documentação.



| Tópico                                                                                                                  | Descrição                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Requisitos gerais para o desenvolvimento de aplicativos](general-requirements-for-application-development.md)               | Requisitos de hardware e software para desenvolver drivers e aplicativos usando Windows Dispositivos Portáteis.     |
| [Requisitos para Windows mídia DRM-Enabled aplicativos](requirements-for-windows-media-drm-enabled-applications.md) | Propriedades que são necessárias para habilitar Windows de conteúdo protegido por DRM de mídia.                      |
| [Amostras](sample.md)                                                                                                  | Descrição de dois aplicativos de área de trabalho de linha de comando fornecidos com este kit de desenvolvimento de software. |
| [Visão geral do aplicativo](application-overview.md)                                                                       | Principais conceitos usados em Windows Dispositivos Portáteis.                                                             |
| [Guia de programação](programming-guide.md)                                                                             | Principais tarefas que um aplicativo executará, com instruções passo a passo e snippets de código.              |
| [Referência de programação](programming-reference.md)                                                                     | Guia de referência para as interfaces e tipos de dados definidos Windows Dispositivos Portáteis.                      |



 

Os aplicativos Windows mídia Gerenciador de Dispositivos ou aquisição de imagem Windows podem acessar Windows Dispositivos Portáteis por meio de uma camada de compatibilidade.

A Microsoft fornece vários drivers para protocolos e dispositivos padrão, incluindo dispositivos MTP (Protocolo de Transporte de Mídia) e dispositivos MSC (Classe Armazenamento Mass). Se você estiver familiarizado com o User-Mode Driver Framework, poderá desenvolver seus próprios drivers para dispositivos personalizados.

 

 



