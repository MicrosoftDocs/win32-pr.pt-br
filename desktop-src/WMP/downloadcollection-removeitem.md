---
title: Método DownloadCollection.removeItem
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método removeItem remove um item de download de uma coleção de download.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- Método removeItem Windows Media Player
- método removeItem Windows Media Player , classe DownloadCollection
- Classe DownloadCollection Windows Media Player , método removeItem
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
ms.openlocfilehash: d1d7eaa7b26a4d64070cae426d1bbc23418593fa8ec5472e870ed7529ce8a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997066"
---
# <a name="downloadcollectionremoveitem-method"></a>Método DownloadCollection.removeItem

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **método removeItem** remove um item de download de uma coleção de download.

## <a name="syntax"></a>Sintaxe


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*itemID* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice do **DownloadItem a** ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o download representado por *itemID* estiver em andamento, esse método cancelará o download.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DownloadCollection.item**](downloadcollection-item.md)
</dt> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> </dl>

 

 





