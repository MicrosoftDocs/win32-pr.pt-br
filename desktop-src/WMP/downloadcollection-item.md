---
title: Método downloadcollection. Item
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método item recupera um objeto de download pendente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método de item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810562"
---
# <a name="downloadcollectionitem-method"></a>Método downloadcollection. Item

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **Item** recupera um objeto de download pendente.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ItemId* \[ no\]
</dt> <dd>

**Número** (**longo**) especificando o índice do **DownloadItem** a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **DownloadItem** .

## <a name="remarks"></a>Comentários

O valor de *ItemId* é baseado em zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto downloadcollection**](downloadcollection-object.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





