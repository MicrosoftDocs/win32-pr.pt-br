---
title: DirectShow e Windows Media
description: DirectShow e Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637140"
---
# <a name="directshow-and-windows-media"></a>DirectShow e Windows Media

Como alternativa ao uso exclusivo do Windows Media Format SDK, os aplicativos também podem ler e gravar o conteúdo baseado no Windows Media usando a arquitetura de streaming do Microsoft® DirectShow®, conforme descrito nas seções a seguir.



| Seção                                                                                   | Descrição                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre o DirectShow](about-directshow.md)                                                  | Descreve o DirectShow em termos gerais e informa onde obter mais informações sobre ele.                                                     |
| [Por que usar o DirectShow?](why-use-directshow.md)                                             | Descreve como o DirectShow simplifica determinadas tarefas na criação e na reprodução de conteúdo baseado no Windows Media.                              |
| [Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)                    | Descreve como reproduzir arquivos ASF usando o DirectShow.                                                                                           |
| [Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)                  | Descreve como criar arquivos ASF usando o DirectShow.                                                                                         |
| [\_Notificação de eventos de status do WMT no DirectShow](wmt-status-notification-in-directshow.md) | Descreve quais eventos de **\_ status de WMT** são tratados pelo leitor de ASF e filtros do gravador ASF e como os aplicativos podem receber esses eventos. |
| [Suporte a DRM no DirectShow](drm-support-in-directshow.md)                                | Descreve como ler e gravar arquivos protegidos por DRM por meio do DirectShow.                                                                     |
| [Referência do QASF do DirectShow](directshow-qasf-reference.md)                                | Contém a documentação de referência para os componentes do DirectShow que dão suporte ao Windows Media.                                              |



 

Três aplicativos de exemplo no SDK ilustram o uso do DirectShow: DSCopy, DSPlay e DSSeekFM. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

> [!Note]  
> Os aplicativos que usam os componentes QASF incluídos neste SDK exigem que o Microsoft DirectX® 8,1 ou o tempo de execução do SDK posterior seja instalado nos sistemas Windows® 2000, Windows 98 e Windows 95. Especificamente, esse tempo de execução é exigido pelo filtro de invólucro do DMO que hospeda os codecs de mídia do Windows em um grafo de filtro do DirectShow.

 

 

 




