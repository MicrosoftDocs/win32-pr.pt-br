---
description: O método item do objeto SWbemPropertySet Obtém um SWbemProperty nomeado da coleção. Este é o método padrão para esse objeto.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171780"
---
# <a name="swbempropertysetitem-method"></a>Método SWbemPropertySet. Item

O método **Item** do objeto [**SWbemPropertySet**](swbempropertyset.md) Obtém um [**SWbemProperty**](swbemproperty.md) nomeado da coleção. Este é o método padrão para esse objeto.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome da propriedade a ser recuperada.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. Esse valor deve ser zero, se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemProperty**](swbemproperty.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Falha não especificada.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749896
</dt> <dd>

Não há memória suficiente para execução deste método.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | ISWbemPropertySet de IID \_<br/>                                                       |



 

 




