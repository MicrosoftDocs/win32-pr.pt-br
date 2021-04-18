---
title: Método downloadcollection. removeItem
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método removeItem remove um item de download de uma coleção de download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- método removeItem Windows Media Player
- método removeItem Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758223"
---
# <a name="downloadcollectionremoveitem-method"></a>Método downloadcollection. removeItem

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **RemoveItem** remove um item de download de uma coleção de download.

## <a name="syntax"></a>Sintaxe


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ItemId* \[ no\]
</dt> <dd>

**Número** (**longo**) especificando o índice do **DownloadItem** a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o download representado por *ItemId* estiver em andamento, esse método cancelará o download.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Downloadcollection. Item**](downloadcollection-item.md)
</dt> <dt>

[**Objeto downloadcollection**](downloadcollection-object.md)
</dt> </dl>

 

 





