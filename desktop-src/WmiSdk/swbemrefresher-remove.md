---
description: O método SWbemRefresher. Remove remove o objeto SWbemRefreshableItem com o índice especificado do atualizador.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Método SWbemRefresher. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930172"
---
# <a name="swbemrefresherremove-method"></a>Método SWbemRefresher. Remove

O método **SWbemRefresher. Remove** remove o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) com o índice especificado do atualizador. O objeto **SWbemRefreshableItem** pode representar um único objeto ou um conjunto de objetos.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LIndex* 
</dt> <dd>

Índice do item no objeto [**SWbemRefresher**](swbemrefresher.md) .

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Os sinalizadores devem ser definidos T0 (zero).

</dd> <dt>

*objWbemNamedvalueSet* \[ adicional\]
</dt> <dd>

Nulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Este método não tem valores de retorno.

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
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemRefresher de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




