---
title: DownloadItem. Size
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade Size recupera o tamanho do download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. dimensionar o Windows Media Player
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
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784902"
---
# <a name="downloaditemsize"></a>DownloadItem. Size

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **size** recupera o tamanho do download.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem. Progress**](downloaditem-progress.md)
</dt> </dl>

 

 





