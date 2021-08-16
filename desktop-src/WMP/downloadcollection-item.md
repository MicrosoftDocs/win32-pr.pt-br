---
title: Método DownloadCollection.item
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método de item recupera um objeto de download pendente.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- método item Windows Media Player
- método item Windows Media Player , classe DownloadCollection
- Classe DownloadCollection Windows Media Player método , item
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
ms.openlocfilehash: 8a82a903236038c2f0372786137eec48ad5c5f502d7fd614eb8944f3f4684aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997035"
---
# <a name="downloadcollectionitem-method"></a>Método DownloadCollection.item

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **método de item** recupera um objeto de download pendente.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*itemId* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice do **DownloadItem a** ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto DownloadItem.**

## <a name="remarks"></a>Comentários

O *valor itemID* é baseado em zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





