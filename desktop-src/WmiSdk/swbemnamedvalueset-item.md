---
description: O método item do objeto SWbemNamedValueSet Obtém um objeto SWbemNamedValue da coleção.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505669"
---
# <a name="swbemnamedvaluesetitem-method"></a>Método SWbemNamedValueSet. Item

O método **Item** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) Obtém um objeto [**SWbemNamedValue**](swbemnamedvalue.md) da coleção.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do valor a recuperar.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. Esse valor deve ser zero, se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemNamedValue**](swbemnamedvalue.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro inválido foi especificado ou o namespace não pôde ser analisado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O item solicitado não foi encontrado.

</dd> </dl>

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

 

 




