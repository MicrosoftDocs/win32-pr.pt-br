---
title: Registro de cores
description: Esses registros de saída do sombreador de vértice contêm um valor de cor.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104297823"
---
# <a name="color-register"></a>Registro de cores

Esses registros de saída do sombreador de vértice contêm um valor de cor. 

| Registre-se | Description              |
|----------|--------------------------|
| oD0      | registro de cores difusas.  |
| oD1      | registro de cor especular. |



 

O valor de oD0 é interpolado e gravado no registro de cor do sombreador de pixel 0 (V0). O valor de oD1 é interpolado e gravado no registro de cor do sombreador de pixel 1 (v1). Para obter mais informações sobre registros de cores do sombreador de pixel, consulte o tópico [registro de cores de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) do sombreador de pixels.

## <a name="remarks"></a>Comentários

Exemplo


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




