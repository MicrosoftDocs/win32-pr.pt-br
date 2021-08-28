---
title: PLAYLIST. @ Media
description: O atributo de mídia recupera o objeto de mídia correspondente ao índice fornecido no elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Windows Media Player de PLAYLIST. multimídia
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746854"
---
# <a name="playlistitemmedia"></a>PLAYLIST. @ Media

O atributo de **mídia** recupera o objeto de **mídia** correspondente ao índice fornecido no elemento **playlist** .

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um objeto de **mídia** somente leitura.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número**(**longo**) que contém o índice de um item da playlist.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **Propriedade do ItemProperty retornará os objetos** de mídia que são expandidos no elemento **playlist** . Por exemplo, se houver uma lista de reprodução que contenha três clipes de mídia que não esteja expandido no elemento **playlist** , o de **mídia**(0) retornará a playlist como o objeto de mídia. Se a lista de reprodução for expandida, o **arquivo** de mídia (0) retornará o primeiro clipe de mídia na lista de reprodução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





