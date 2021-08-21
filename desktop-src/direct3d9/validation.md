---
description: A validação é executada durante a compilação do efeito. Para validar a técnica atual, especifique NULL como o alça de técnica a ser validado.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d6c49f3bdf3bc0ba75f52bd8138fa6f5d777c3613d105b2706929c01b3ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519434"
---
# <a name="validation-direct3d-9"></a>Validação (Direct3D 9)

A validação é executada durante a compilação do efeito. Para validar a técnica atual, **especifique NULL** como o alça de técnica a ser validado.

A validação falhará para qualquer um dos seguintes:

-   Se o alça de técnica especificado não existir.
-   Se a aplicação de qualquer estado em qualquer passagem da técnica falhar.
-   Se a validação do dispositivo falhar após a aplicação de todos os estados em qualquer passagem da técnica.
-   Se os estados de efeito PIXELSHADER ou VERTEXSHADER são atribuídos sombreadores inválidos em qualquer passagem da técnica.
-   Se os limites do dispositivo não oferecerem suporte ao mapeamento de cubo e um estado de efeito TEXTURE for atribuído a um valor do tipo textureCUBE em qualquer passagem da técnica.
-   Se os limites do dispositivo não deem suporte ao mapeamento de volume e um estado de efeito TEXTURE for atribuído a um valor do tipo texture3D em qualquer passagem da técnica.

Para obter mais informações, consulte [Estados de efeito (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



