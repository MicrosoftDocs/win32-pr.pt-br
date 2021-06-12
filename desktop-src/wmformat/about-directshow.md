---
title: Saiba mais sobre o DirectShow no SDK do Windows Media Format 11, uma arquitetura de streaming de dados de alto nível, modular, extensível para a plataforma Windows.
description: Sobre o DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow,sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011289"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Sobre o DirectShow (Windows Media Format SDK 11)

O DirectShow é uma arquitetura de streaming de dados de alto nível, modular, extensível para a plataforma Windows. Ele fornece os componentes de software subjacentes e as APIs (interfaces de programação de aplicativo) para uma ampla variedade de aplicativos digitais de áudio e vídeo no mercado atualmente. O DirectShow está disponível como parte do Microsoft DirectX Software Development Kit. Para saber mais sobre o DirectShow, confira o SDK da Plataforma Microsoft.

No DirectShow, todos os componentes de streaming de dados são chamados de *filtros*. Um filtro pode representar um dispositivo de hardware, um codificador ou decodificador de software, um renderador de áudio ou vídeo ou qualquer capacidade de processamento de áudio e vídeo. Para permitir que aplicativos baseados em DirectShow leiam e escrevam conteúdo Windows Media Format, incluindo conteúdo protegido pelo DRM (Digital Rights Management), a Microsoft fornece dois filtros que encapsulam partes do SDK do Windows Media Format. Estes são o [Leitor do WM ASF](wm-asf-reader-filter.md) e o [Wm ASF Writer.](wm-asf-writer-filter.md) Esses filtros e as interfaces que eles expõem são coletivamente chamados de componentes qaSF, após a DLL na qual eles são empacotados. (O Q significa Ltda, um nome de código antecipado para DirectShow.)

> [!Note]  
> O uso dos codecs do Windows Media Audio and Video 9 Series por meio dos componentes qaSF do DirectShow requer o Microsoft Windows Millennium Edition ou posterior ou o DirectX 8.0 ou posterior.

 

O diagrama a seguir mostra um grafo de filtro do DirectShow para reprodução de arquivos de Vídeo de Mídia do Windows.

![grafo de reprodução de vídeo de mídia do Windows](images/wmv-wmasfreader.png)

O [Leitor do WM ASF](wm-asf-reader-filter.md) é um componente qaSF, os decodificadores são componentes do SDK do Windows Media Format hospedados no filtro wrapper do DMO (um componente QASF) e os renderadores são componentes do DirectShow.

 

 




