---
description: A classe CImagePalette gerencia paletas para renderizadores de vídeo. Ele pode ser usado para criar uma paleta lógica a partir de um formato de vídeo. Essa classe destina-se a ser usada com as classes CBaseWindow e CDrawImage, portanto, é um pouco especializada.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Classe CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 390bd4fc60e7d20264ae3a9238699108e7778524b73c6af22038197260da4463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074060"
---
# <a name="cimagepalette-class"></a>Classe CImagePalette

A `CImagePalette` classe gerencia paletas para renderizadores de vídeo. Ele pode ser usado para criar uma paleta lógica a partir de um formato de vídeo. Essa classe destina-se a ser usada com as classes [**CBaseWindow**](cbasewindow.md) e [**CDrawImage**](cdrawimage.md) , portanto, é um pouco especializada.



| Variáveis de membro protegido                                       | Descrição                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**\_hPalette m**](cimagepalette-m-hpalette.md)                  | Identificador para a paleta lógica que este objeto gerencia.                                        |
| [**\_pBaseWindow m**](cimagepalette-m-pbasewindow.md)            | Ponteiro para o objeto **CBaseWindow** que gerencia a janela.                                 |
| [**\_pDrawImage m**](cimagepalette-m-pdrawimage.md)              | Ponteiro para o objeto **CDrawImage** que desenha a imagem de vídeo.                               |
| [**\_pFilter m**](cimagepalette-m-pfilter.md)                    | Ponteiro para o filtro proprietário.                                                                  |
| Métodos públicos                                                   | Descrição                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Método de construtor.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Copia a paleta de qualquer estrutura **VIDEOINFO** para qualquer estrutura **VIDEOINFO** palettized. |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Tenta criar uma paleta que mapeia diretamente para a paleta selecionada no dispositivo de vídeo.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Cria uma paleta lógica da tabela de cores em um formato de vídeo.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Configura uma paleta, com base em um tipo de mídia do filtro proprietário.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Exclui a paleta lógica existente.                                                          |



 

 

 



