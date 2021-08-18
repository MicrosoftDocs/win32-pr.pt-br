---
title: DownloadItem.size
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade size recupera o tamanho do download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem.size Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 046c48cc324b8d388d9f730dc3ed4d6739632d169d02d11c77201fe1da3e98c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749717"
---
# <a name="downloaditemsize"></a>DownloadItem.size

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade** size recupera o tamanho do download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem.progress**](downloaditem-progress.md)
</dt> </dl>

 

 





