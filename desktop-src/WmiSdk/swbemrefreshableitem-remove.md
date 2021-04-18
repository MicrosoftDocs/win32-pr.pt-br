---
description: O método SWbemRefreshableItem. Remove remove o objeto SWbemRefreshableItem do objeto pai SWbemRefresher. Objeto SWbemRefreshableItem do objeto SWbemRefresher pai.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Método SWbemRefreshableItem. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785023"
---
# <a name="swbemrefreshableitemremove-method"></a>Método SWbemRefreshableItem. Remove

O método **SWbemRefreshableItem. Remove** remove o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) do objeto pai [**SWbemRefresher**](swbemrefresher.md) .

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ em, opcional\]
</dt> <dd>

Esse parâmetro deve ser definido como 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

**Códigos de erro** Se o atualizador não tiver nenhum item com o índice especificado, **wbemErrNotFound** será gerado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHABLEITEM CLSID<br/>                                                  |
| IID<br/>                      | ISWbemRefreshableItem de IID \_<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




