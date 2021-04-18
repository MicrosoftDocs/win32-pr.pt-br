---
description: A validação é executada durante o efeito compilar. Para validar a técnica atual, especifique NULL como o identificador de técnica a ser validado.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808221"
---
# <a name="validation-direct3d-9"></a>Validação (Direct3D 9)

A validação é executada durante o efeito compilar. Para validar a técnica atual, especifique **NULL** como o identificador de técnica a ser validado.

A validação falhará para qualquer um dos seguintes:

-   Se o identificador de técnica especificado não existir.
-   Se o aplicativo de qualquer estado em qualquer passagem da técnica falhar.
-   Se a validação do dispositivo falhar após a aplicação de todos os Estados em qualquer passagem da técnica.
-   Se os Estados de efeito PIXELSHADER ou VERTEXSHADER forem atribuídos a sombreadores inválidos em qualquer passagem da técnica.
-   Se as tampas do dispositivo não oferecerem suporte ao mapeamento de cubo, e um estado de efeito de textura for atribuído a um valor do tipo textureCUBE em qualquer passagem da técnica.
-   Se as tampas do dispositivo não dão suporte ao mapeamento de volume e um estado de efeito de textura é atribuído a um valor do tipo texture3D em qualquer passagem da técnica.

Para obter mais informações, consulte [Estados de efeito (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



