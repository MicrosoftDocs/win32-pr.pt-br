---
title: Funções de formato de pixel
description: As funções do Windows a seguir gerenciam formatos de pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funções WGL, formato de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823002"
---
# <a name="pixel-format-functions"></a>Funções de formato de pixel

As funções do Windows a seguir gerenciam formatos de pixel.



| Função do Windows                                               | Descrição                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Obtém o formato de pixel do contexto do dispositivo que é a correspondência mais próxima a um formato de pixel especificado.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Define o formato de pixel atual de um contexto de dispositivo para o formato de pixel especificado por um índice de formato de pixel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Obtém o índice de formato de pixel do formato de pixel atual de um contexto de dispositivo.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Dado um contexto de dispositivo e um índice de formato de pixel, preenche uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) com as propriedades do formato de pixel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Recupera informações de formato de pixel para um metarquivo avançado.                                                                                                          |



 

A função [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) retorna um índice de formato de pixel baseado em um que identifica a melhor correspondência dos formatos de pixel com suporte do contexto do dispositivo.

A função [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica o formato desejado usando um índice de formato de pixel baseado em um. Normalmente, você chama **ChoosePixelFormat** para encontrar um formato de pixel de melhor correspondência e, em seguida, chamar **SetPixelFormat** com o resultado de **ChoosePixelFormat**.

Se você chamar **SetPixelFormat** para um contexto de dispositivo que faz referência a uma janela, **SetPixelFormat** também alterará o formato de pixel da janela. Definir o formato de pixel de uma janela mais de uma vez pode levar a complicações significativas para o Gerenciador de janelas e para aplicativos multithread, portanto, não é permitido. Você pode definir o formato de pixel de uma janela somente uma vez; Depois disso, o formato de pixel da janela não pode ser alterado.

A função [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) retorna um índice de formato de pixel baseado em um.

A função [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) usa o seguinte como parâmetros:

-   Um identificador para um contexto de dispositivo
-   Um índice de formato de pixel
-   Um ponteiro para uma estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

A função [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) retorna com os membros de **PIXELFORMATDESCRIPTOR** definidos adequadamente.

A função **GetEnhMetaFilePixelFormat** retorna o tamanho do formato de pixel de um metarquivo e recupera as informações de formato de pixel do metarquivo.

 

 




