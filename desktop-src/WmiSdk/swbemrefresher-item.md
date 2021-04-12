---
description: O método SWbemRefresher. Item retorna o SWbemRefreshableItem especificado da coleção. SWbemRefreshableItem da coleção.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Método SWbemRefresher. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172478"
---
# <a name="swbemrefresheritem-method"></a>Método SWbemRefresher. Item

O método **SWbemRefresher. Item** retorna o [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado da coleção.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* 
</dt> <dd>

Valor de índice do item na coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a chamada for bem-sucedida, o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) especificado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Se o atualizador não tiver nenhum item com o índice especificado, **wbemErrNotFound** será gerado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemRefresher de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




