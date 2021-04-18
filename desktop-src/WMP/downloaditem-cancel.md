---
title: Método DownloadItem. Cancel
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método Cancel cancela o download.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancelar método Windows Media Player
- método Cancel Windows Media Player, classe DownloadItem
- Classe DownloadItem do Windows Media Player, método Cancel
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
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760455"
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

## <a name="return-value"></a>Retornar valor

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

 

 





