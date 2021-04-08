---
title: Sobre o DirectShow (SDK do Windows Media Format 11)
description: Sobre o DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008749"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Sobre o DirectShow (SDK do Windows Media Format 11)

O DirectShow é uma arquitetura de streaming de dados de alto nível, modular e extensível para a plataforma Windows. Ele fornece componentes de software subjacentes e APIs (interfaces de programação de aplicativo) para uma ampla variedade de aplicativos de áudio e vídeo digital no mercado atualmente. O DirectShow está disponível como parte do Microsoft DirectX Software Development Kit. Para saber mais sobre o DirectShow, consulte o SDK da plataforma Microsoft.

No DirectShow, todos os componentes de streaming de dados são chamados de *filtros*. Um filtro pode representar um dispositivo de hardware, um codificador ou decodificador de software, um processador de áudio ou vídeo ou qualquer recurso de processamento de vídeo de áudio. Para permitir que aplicativos baseados no DirectShow leiam e gravem conteúdo de formato de mídia do Windows, incluindo conteúdo protegido por DRM (Rights Management digital), a Microsoft fornece dois filtros que encapsulam partes do SDK do Windows Media Format. Esses são os [leitores ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md). Esses filtros e as interfaces que eles expõem são coletivamente chamados de componentes QASF, após a DLL na qual eles são empacotados. (O Q significa o Quartz, um nome de código inicial para o DirectShow.)

> [!Note]  
> O uso dos codecs do Windows Media Audio e vídeo 9 Series por meio dos componentes do QASF do DirectShow requer o Microsoft Windows Millennium Edition ou posterior, ou o DirectX 8,0 ou posterior.

 

O diagrama a seguir mostra um grafo de filtro do DirectShow para reproduzir arquivos de vídeo de mídia do Windows.

![Grafo de reprodução de vídeo do Windows Media](images/wmv-wmasfreader.png)

O [leitor de ASF do WM](wm-asf-reader-filter.md) é um componente do QASF, os decodificadores são componentes do Windows Media Format SDK hospedados no filtro de invólucro do DMO (um componente QASF) e os renderizadores são componentes do DirectShow.

 

 




