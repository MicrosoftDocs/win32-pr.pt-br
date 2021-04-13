---
description: Usado para definir a topologia de textura de cada face em um encapsulamento. O valor do membro nFaceWrapValues deve ser igual ao número de faces em uma malha.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500158"
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

 

 



