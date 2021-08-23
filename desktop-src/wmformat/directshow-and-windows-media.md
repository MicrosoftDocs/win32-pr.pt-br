---
title: DirectShow e Windows mídia
description: DirectShow e Windows mídia
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows SDK de formato de mídia, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027904"
---
# <a name="directshow-and-windows-media"></a>DirectShow e Windows mídia

Como alternativa ao uso exclusivo do SDK de Formato de Mídia do Windows, os aplicativos também podem ler e gravar conteúdo baseado em mídia do Windows usando ® DirectShow® arquitetura de streaming da Microsoft, conforme descrito nas seções a seguir.



| Seção                                                                                   | Descrição                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre DirectShow](about-directshow.md)                                                  | Descreve DirectShow em termos gerais e informa onde obter mais informações sobre ele.                                                     |
| [Por que usar DirectShow?](why-use-directshow.md)                                             | Descreve como DirectShow simplifica determinadas tarefas na criação e reprodução de Windows conteúdo baseado em mídia.                              |
| [Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)                    | Descreve como reproduzir arquivos ASF usando DirectShow.                                                                                           |
| [Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)                  | Descreve como criar arquivos ASF usando DirectShow.                                                                                         |
| [Notificação de \_ evento WMT STATUS no DirectShow](wmt-status-notification-in-directshow.md) | Descreve quais eventos **DE \_ STATUS do WMT** são tratados pelos filtros Leitor do ASF e AsF Writer e como os aplicativos podem receber esses eventos. |
| [Suporte a DRM no DirectShow](drm-support-in-directshow.md)                                | Descreve como ler e gravar arquivos protegidos por DRM por meio DirectShow.                                                                     |
| [DirectShow Referência de QASF](directshow-qasf-reference.md)                                | Contém a documentação de referência para os DirectShow que suportam Windows Mídia.                                              |



 

Três aplicativos de exemplo no SDK ilustram o uso de DirectShow: DSCopy, DSPlay e DSSeekFM. Para obter mais informações, consulte [Aplicativos de exemplo](sample-applications.md).

> [!Note]  
> Os aplicativos que usam os componentes qaSF incluídos neste SDK exigem que o runtime do SDK do Microsoft DirectX® 8.1 ou posterior seja instalado nos sistemas Windows® 2000, Windows 98 e Windows 95. Especificamente, esse runtime é exigido pelo filtro DMO Wrapper, que hospeda os codecs Windows Media em um grafo DirectShow filtro.

 

 

 




