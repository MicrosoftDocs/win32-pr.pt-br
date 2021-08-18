---
title: Elemento COPYRIGHT (Msfeeds.h)
description: O elemento COPYRIGHT define uma cadeia de caracteres de texto que especifica as informações de direitos autorais para um elemento ASX ou ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5a01e97364aa47182e38e3e3066895c771e2d5edb6c480e8108cb168e7f8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997456"
---
# <a name="copyright-element"></a>Elemento COPYRIGHT

O **elemento COPYRIGHT** define uma cadeia de caracteres de texto que especifica as informações de direitos autorais para um elemento **ASX** **ou ENTRY.**

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **ASX**, **ENTRY** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma cadeia de caracteres de texto que especifica as informações de direitos autorais para um **elemento ASX** **ou ENTRY.**

Quando esse elemento aparece em um **elemento ASX,** a cadeia de caracteres de direitos autorais é exibida apenas como **Mostrar** informações. Quando esse elemento aparece dentro de **um elemento ENTRY,** o texto é exibido como informações de clipe. Cada elemento **PAI ASX** e **ENTRY** deve conter no máximo um elemento **COPYRIGHT** filho. Vários **elementos COPYRIGHT** após o primeiro serão ignorados e não serão exibidos.

Os caracteres para símbolos de registro de marcas e direitos autorais ( ou ) poderão não ser exibidos corretamente se o metadado não estiver codificado usando o esquema de codificação UTF-8. Nesse caso, para exibir qualquer um desses símbolos corretamente para todos os usuários, você pode usar os equivalentes ASCII (c) e (R) em vez disso.

Se o metadado for codificado usando UTF-8, os símbolos de direitos autorais e marcas comerciais serão exibidos corretamente.

## <a name="examples"></a>Exemplos


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/>                                 |
| Cabeçalho<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando caracteres de direitos autorais a metadados**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





