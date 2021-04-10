---
description: O método remove do objeto SWbemPropertySet exclui uma propriedade da coleção SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091286"
---
# <a name="swbempropertysetremove-method"></a>Método SWbemPropertySet. Remove

O método **Remove** do objeto [**SWbemPropertySet**](swbempropertyset.md) exclui uma propriedade da coleção **SWbemPropertySet** .

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do item a ser removido.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. Esse valor deve ser 0 (zero) se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Falha não especificada.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

O usuário tentou excluir uma propriedade que não pode ser excluída.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

A propriedade especificada não existe.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para execução deste método.

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380)
</dt> <dd>

O usuário tentou excluir uma propriedade que não era de propriedade. A propriedade foi herdada de uma classe pai.

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002)
</dt> <dd>

O usuário excluiu um valor padrão de substituição para a classe atual. O valor padrão para essa propriedade na classe pai foi reativado.

</dd> </dl>

## <a name="remarks"></a>Comentários

As propriedades não podem ser removidas de instâncias de classe ou classes derivadas com propriedades herdadas. Essas tentativas de exclusão geram um erro e a propriedade não é removida; a propriedade é redefinida para seu valor padrão.

Não é possível iterar uma coleção durante a remoção de itens porque, quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo de código que usa esse método, consulte o tópico [**SWbemPropertySet**](swbempropertyset.md) .

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




