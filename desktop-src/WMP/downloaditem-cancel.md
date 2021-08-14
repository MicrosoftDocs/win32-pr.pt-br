---
title: Método DownloadItem. Cancel
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Cancel cancela o download.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- Windows Media Player do método Cancel
- método cancel Windows Media Player, classe DownloadItem
- classe DownloadItem Windows Media Player, método cancel
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6208719b5ac2e81fb9175db9de67bcf1f00ad7c34787ed1ab45251abd517bd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749727"
---
# <a name="downloaditemcancel-method"></a>Método DownloadItem. Cancel

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **Cancel** cancela o download.

## <a name="syntax"></a>Sintaxe


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os itens cancelados não são removidos da coleção de download. Os itens cancelados retornam um valor de **downloadstate** de 4 (cancelado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem. downloadstate**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





