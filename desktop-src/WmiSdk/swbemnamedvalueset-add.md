---
description: O método Add do objeto SWbemNamedValueSet adiciona um objeto SWbemNamedValue à coleção. Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet.Add (Wbemdisp.h)
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
ms.openlocfilehash: a7a911dcfa6371421fd4033524400d0c818e814d3bd52f90b677ac7c9fcf1b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612116"
---
# <a name="swbemnamedvaluesetadd-method"></a>Método SWbemNamedValueSet.Add

O **método** Add do [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) adiciona um [**objeto SWbemNamedValue**](swbemnamedvalue.md) à coleção. Se um elemento já existir na coleção com o mesmo nome, o novo elemento o substituirá.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

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

*strName* \[ Em\]
</dt> <dd>

Obrigatórios. Nome do novo valor.

</dd> <dt>

*varVal* \[ Em\]
</dt> <dd>

Obrigatórios. Variante que representa o novo valor.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado e deve ser definido como zero, se especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, esse método retornará o objeto [**SWbemNamedValue**](swbemnamedvalue.md) recém-modificado ou recém-criado.

## <a name="remarks"></a>Comentários

Para exemplos de adição e recuperação de valores nomeados, consulte [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




