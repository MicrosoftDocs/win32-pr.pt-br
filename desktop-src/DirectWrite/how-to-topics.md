---
title: Tópicos de instruções (DirectWrite)
description: veja os tópicos de instruções no guia de programação da API de DirectWrite. DirectWrite permite que Windows aplicativos aprimorem a experiência de texto para a interface do usuário e documentos.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42848fbf00e099926763f0db54338f3a87ff583782b939f8250a1aabb2b73ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048856"
---
# <a name="how-to-topics-directwrite"></a>Tópicos de instruções (DirectWrite)

os tópicos a seguir fornecem uma visão geral da API do [DirectWrite](direct-write-portal.md) .

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como alinhar texto](how-to-align-text.md)<br/>                                                                                                                   | você pode alinhar [DirectWrite](direct-write-portal.md) texto usando o método [**settextalign**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) da interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Como adicionar suporte para vários monitores](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | o [DirectWrite](direct-write-portal.md) inclui suporte para sistemas com vários monitores. Monitores diferentes podem ter uma geometria de pixel diferente (RGB, BGR ou simples) ou outros atributos. Para obter mais informações sobre a geometria de pixel, consulte o tópico de referência de [**\_ \_ geometria de pixel DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . este tópico mostrará como adicionar suporte para vários monitores ao seu aplicativo DirectWrite. <br/> |
| [Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Descreve como criar uma janela que o exibe corretamente em monitores de alto DPI.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Como garantir que o texto seja exibido com a direção de leitura correta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Algumas linguagens, como árabe e Hebraico, exigem uma direção de leitura da direita para a esquerda. o para um objeto de formato de texto [DirectWrite](direct-write-portal.md) , a direção de leitura padrão é da esquerda para a direita. DirectWrite não infere automaticamente a direção de leitura da localidade, portanto, você deve fazer isso por conta própria.<br/>                                                                                                   |
| [Como enumerar fontes](font-enumeration.md)<br/>                                                                                                               | Esta visão geral mostrará como enumerar as fontes na coleção de fontes do sistema, por nome da família.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Como executar testes de clique em um layout de texto](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | fornece um breve tutorial sobre como adicionar testes de clique a um aplicativo [DirectWrite](direct-write-portal.md) que exibe o texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                  |
| [Como adicionar objetos embutidos a um layout de texto](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | fornece um breve tutorial sobre como adicionar objetos embutidos a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                         |
| [Como adicionar efeitos de desenho de cliente a um layout de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | fornece um breve tutorial sobre como adicionar efeitos de desenho de cliente a um aplicativo [DirectWrite](direct-write-portal.md) que exibe texto usando a interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e um processador de texto personalizado. <br/>                                                                                                                                                                                      |



 

 

