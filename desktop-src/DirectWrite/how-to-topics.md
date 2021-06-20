---
title: Tópicos de ida (DirectWrite)
description: Veja os tópicos de ida e volta no guia de programação da API directWrite. O DirectWrite permite que os aplicativos do Windows aprimoram a experiência de texto para a interface do usuário e documentos.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc35d9b92001bc8c4807f8b77434559994aaac4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406389"
---
# <a name="how-to-topics-directwrite"></a>Tópicos de ida (DirectWrite)

Os tópicos a seguir fornecem uma visão geral da API [directWrite.](direct-write-portal.md)

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como alinhar texto](how-to-align-text.md)<br/>                                                                                                                   | Você pode alinhar [o texto directWrite](direct-write-portal.md) usando o [**método SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Como adicionar suporte para vários monitores](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [O DirectWrite](direct-write-portal.md) inclui suporte para sistemas com vários monitores. Monitores diferentes podem ter geometria de pixel diferente (RGB, BGR ou FLAT) ou outros atributos. Para obter mais informações sobre geometria de pixel, consulte o [**tópico referência DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) Este tópico mostrará como adicionar suporte para vários monitores ao seu aplicativo DirectWrite. <br/> |
| [Como garantir que seu aplicativo seja exibido corretamente em exibições de alto DPI](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Descreve como criar uma janela que é exibida corretamente em exibições de alto DPI.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Como garantir que o texto seja exibido com a direção de leitura correta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Alguns idiomas, como árabe e hebraico, exigem uma direção de leitura da direita para a esquerda. O para um objeto de formato de texto [DirectWrite,](direct-write-portal.md) a direção de leitura padrão é da esquerda para a direita. DirectWrite não infere automaticamente a direção de leitura da localidade, portanto, você deve fazer isso por conta própria.<br/>                                                                                                   |
| [Como enumerar fontes](font-enumeration.md)<br/>                                                                                                               | Esta visão geral mostrará como enumerar as fontes na coleção de fontes do sistema, por nome de família.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Como executar testes de acerto em um layout de texto](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Fornece um breve tutorial sobre como adicionar testes de impacto a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                  |
| [Como adicionar objetos em linha a um layout de texto](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Fornece um breve tutorial sobre como adicionar objetos em linha a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                         |
| [Como adicionar efeitos de desenho do cliente a um layout de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Fornece um breve tutorial sobre como adicionar efeitos de desenho do cliente a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e um renderização de texto personalizado. <br/>                                                                                                                                                                                      |



 

 

