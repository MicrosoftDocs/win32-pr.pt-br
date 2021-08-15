---
title: modificadores de registro de origem ps \_ \_ 1 4 para texld, texcrd
description: Instruções de endereço de textura do sombreador de dois pixels versão \_ 1 4, texld – ps \_ \_ 14 e texcrd – ps, têm sintaxe personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63a0cfd212767a0219af83d734d3562edacc84901098afcf77c786d8895f32d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512872"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>modificadores de registro de origem ps \_ \_ 1 4 para texld, texcrd

As instruções de endereço de textura do sombreador de dois pixels versão \_ 1 4, [texld - ps \_ \_ 1 4](texld---ps-1-4.md) e [texcrd - ps](texcrd---ps.md), têm sintaxe personalizada. Essas instruções suportam seu próprio conjunto de modificadores de registro de origem, seletores de registro de origem e máscaras de gravação de registro de destino, conforme mostrado aqui.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificadores de registro de origem para texld e texcrd

Esses modificadores fornecem a funcionalidade de divisão projetiva dividindo os valores x e y pelos valores z ou w.



| Modificadores de registro de origem | Descrição                | Syntax       |
|---------------------------|----------------------------|--------------|
| \_Dz                      | Dividir componentes x,y por z | register \_ dz |
| \_db                      | Dividir componentes x,y por z | registrar \_ banco de dados |
| \_Dw                      | Dividir componentes x,y por w | register \_ dw |
| \_da                      | Dividir componentes x,y por w | register \_ da |



 

### <a name="remarks"></a>Comentários

O \_ modificador dz \_ ou db faz o seguinte:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



O \_ modificador \_ dw ou da faz o seguinte:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




