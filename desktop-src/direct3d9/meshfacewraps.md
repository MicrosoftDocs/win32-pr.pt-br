---
description: Usado para definir a topologia de textura de cada face em um encapsulamento. O valor do membro nFaceWrapValues deve ser igual ao número de faces em uma malha.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0878754b9e9e58e0f508be26ab30ac44112b1a2e8d8ba0f7e597591b2ebdab81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746966"
---
# <a name="meshfacewraps"></a>MeshFaceWraps

Usado para definir a topologia de textura de cada face em um encapsulamento. O valor do membro nFaceWrapValues deve ser igual ao número de faces em uma malha.

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

Este modelo não é mais usado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



