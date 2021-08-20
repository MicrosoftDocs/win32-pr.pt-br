---
title: Funções de formato de pixel
description: As funções Windows a seguir gerenciam formatos de pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funções WGL, formato de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c4b82a2b6cd91dd007cecf78065fa0c01204ecf468017ec7e121bd764c9ff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486326"
---
# <a name="pixel-format-functions"></a>Funções de formato de pixel

As funções Windows a seguir gerenciam formatos de pixel.



| Windows Função                                               | Descrição                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EscolhaPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Obtém o formato de pixel do contexto do dispositivo que é a mais próxima de um formato de pixel especificado.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Define o formato de pixel atual de um contexto de dispositivo para o formato de pixel especificado por um índice de formato de pixel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Obtém o índice de formato de pixel do formato de pixel atual de um contexto de dispositivo.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Dado um contexto de dispositivo e um índice de formato de pixel, preenche uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) com as propriedades do formato de pixel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Recupera informações de formato de pixel para um metarquivo aprimorado.                                                                                                          |



 

A [**função ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) retorna um índice de formato de pixel baseado em um que identifica a melhor combinação dos formatos de pixel com suporte do contexto do dispositivo.

A [**função SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica o formato desejado usando um índice de formato de pixel baseado em um. Normalmente, você chama **ChoosePixelFormat** para encontrar um formato de pixel de melhor combinação e, em seguida, chama **SetPixelFormat** com o resultado de **ChoosePixelFormat**.

Se você chamar **SetPixelFormat para** um contexto de dispositivo que faz referência a uma janela, **SetPixelFormat** também altera o formato de pixel da janela. Definir o formato de pixel de uma janela mais de uma vez pode levar a complicações significativas para o Gerenciador de Janelas e para aplicativos multithread, portanto, isso não é permitido. Você pode definir o formato de pixel de uma janela apenas uma vez; Depois disso, o formato de pixel da janela não pode ser alterado.

A [**função GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) retorna um índice de formato de pixel baseado em um.

A [**função DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) assume o seguinte como parâmetros:

-   Um handle para um contexto de dispositivo
-   Um índice de formato de pixel
-   Um ponteiro para uma [**estrutura de dados PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

A [**função DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) retorna com os membros de **PIXELFORMATDESCRIPTOR** definidos adequadamente.

A **função GetEnhMetaFilePixelFormat** retorna o tamanho do formato de pixel de um metarquivo e recupera as informações de formato de pixel do metarquivo.

 

 




