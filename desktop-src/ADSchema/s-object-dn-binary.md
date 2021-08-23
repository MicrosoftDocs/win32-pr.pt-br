---
title: Sintaxe object(DN-Binary)
description: Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome diferenciado).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema do AD de sintaxe object(DN-Binary)
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15172a8577cf8ccec71053c3d374b389d71d3264fcc1934b19440a3f9efc4904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702565"
---
# <a name="objectdn-binary-syntax"></a>Sintaxe object(DN-Binary)

Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome diferenciado).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------------------|
| Nome         | Object(DN-Binary)                                                                  |
| ID da sintaxe    | 2.5.5.7                                                                            |
| OM ID        | 127                                                                                |
| Tipo MAPI    | TSTRING                                                                            |
| Tipo ADS     | ADSTYPE \_ DN \_ COM \_ BINÁRIO                                                          |
| Tipo de variante | DISPATCH \_ da VT                                                                       |
| Tipo de SDS     | Um objeto COM que pode ser lançado em [**um IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary). |



## <a name="remarks"></a>Comentários

Um valor com essa sintaxe tem o seguinte formato:

``` syntax
B:<char count>:<binary value>:<object DN>
```

em que " contagem de caracteres " é o número de dígitos hexadecimais em " valor binário ", " valor binário " é a representação &lt; &gt; &lt; &gt; &lt; &gt; hexadecimal &lt; do valor binário e " DN de objeto &gt; " é um nome diferenciado. O Active Directory atualizará automaticamente o DN se o objeto ao qual ele se refere for movido ou renomeado. Para obter mais informações e um exemplo de código que usa essa sintaxe, consulte Habilitando a associação rename-safe com a [outra propriedadeWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
