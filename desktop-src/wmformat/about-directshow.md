---
title: Saiba mais DirectShow no SDK do Windows Media Format 11, uma arquitetura de streaming de dados de alto nível, modular, extensível para a plataforma Windows.
description: Sobre DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows SDK de formato de mídia, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840402"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Sobre DirectShow (SDK Windows Media Format 11)

DirectShow é uma arquitetura de streaming de dados de alto nível, modular, extensível para a Windows plataforma. Ele fornece os componentes de software subjacentes e as APIs (interfaces de programação de aplicativo) para uma ampla variedade de aplicativos digitais de áudio e vídeo no mercado atualmente. DirectShow está disponível como parte do Microsoft DirectX Software Development Kit. Para saber mais sobre o DirectShow, confira o SDK da Microsoft Platform.

No DirectShow, todos os componentes de streaming de dados são chamados de *filtros*. Um filtro pode representar um dispositivo de hardware, um codificador ou decodificador de software, um renderador de áudio ou vídeo ou qualquer capacidade de processamento de áudio e vídeo. Para permitir que aplicativos baseados em DirectShow leiam e escrevam conteúdo de Formato de Mídia do Windows, incluindo conteúdo protegido pelo DRM (Digital Rights Management), a Microsoft fornece dois filtros que encapsulam partes do SDK de Formato de Mídia Windows. Estes são o [Leitor do WM ASF](wm-asf-reader-filter.md) e o [Wm ASF Writer.](wm-asf-writer-filter.md) Esses filtros e as interfaces que eles expõem são coletivamente chamados de componentes qaSF, após a DLL na qual eles são empacotados. (O Q significa Ltda, um nome de código antecipado para DirectShow.)

> [!Note]  
> O uso dos codecs Windows Media Audio e Video 9 series por meio dos componentes DirectShow QASF requer o Microsoft Windows Millennium Edition ou posterior ou DirectX 8.0 ou posterior.

 

O diagrama a seguir mostra um DirectShow de filtros para reprodução Windows de vídeo de mídia.

![grafo de reprodução de vídeo de mídia do Windows](images/wmv-wmasfreader.png)

O [Leitor do WM ASF](wm-asf-reader-filter.md) é um componente qaSF, os decodificadores são componentes do SDK de Formato de Mídia Windows hospedados no filtro wrapper do DMO (um componente QASF) e os renderadores são DirectShow componentes.

 

 




