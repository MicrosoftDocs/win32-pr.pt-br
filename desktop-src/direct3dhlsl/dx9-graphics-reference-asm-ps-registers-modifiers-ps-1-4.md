---
title: '\_ \_ modificadores de registro de origem PS 1 4 para texld, texcrd'
description: Duas instruções de endereço de textura de sombreador de pixel versão 1 \_ 4, texld-PS \_ 1 \_ 4 e texcrd-PS, têm sintaxe personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104084293"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>\_ \_ modificadores de registro de origem PS 1 4 para texld, texcrd

Duas instruções de endereço de textura de sombreador de pixel versão 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) e [texcrd-PS](texcrd---ps.md), têm sintaxe personalizada. Essas instruções dão suporte a seu próprio conjunto de modificadores de registro de origem, seletores de registro de origem e máscaras de gravação de registro de destino, como mostrado aqui.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificadores de registro de origem para texld e texcrd

Esses modificadores fornecem funcionalidade de divisão projetada dividindo os valores x e y pelos valores z ou w.



| Modificadores de registro de origem | Descrição                | Syntax       |
|---------------------------|----------------------------|--------------|
| \_DZ                      | Dividir os componentes x, y por z | registrar \_ DZ |
| \_db                      | Dividir os componentes x, y por z | registrar \_ BD |
| \_dw                      | Dividir os componentes x, y por w | registrar \_ DW |
| \_auditoria                      | Dividir os componentes x, y por w | registrar \_ da |



 

### <a name="remarks"></a>Comentários

O \_ \_ modificador DZ ou DB faz o seguinte:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



O \_ modificador DW ou o \_ da é o seguinte:


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

 

 




