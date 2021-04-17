---
description: O método Add do objeto SWbemNamedValueSet adiciona um objeto SWbemNamedValue à coleção. Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505670"
---
# <a name="swbemnamedvaluesetadd-method"></a>Método SWbemNamedValueSet. Add

O método **Add** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) adiciona um objeto [**SWbemNamedValue**](swbemnamedvalue.md) à coleção. Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do novo valor.

</dd> <dt>

*varVal* \[ no\]
</dt> <dd>

Obrigatórios. Variant que representa o novo valor.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado e deve ser definido como zero se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará o objeto [**SWbemNamedValue**](swbemnamedvalue.md) recém modificado ou recém-criado.

## <a name="remarks"></a>Comentários

Para obter exemplos de como adicionar e recuperar valores nomeados, consulte [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMNAMEDVALUESET CLSID<br/>                                                    |
| IID<br/>                      | ISWbemNamedValueSet de IID \_<br/>                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




