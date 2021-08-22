---
description: O método remove do objeto SWbemQualifierSet exclui um qualificador nomeado da coleção.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f4ca62276e39822964d33b58345b4718354bfd63039ec42ab30ac5daf95f6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463606"
---
# <a name="swbemqualifiersetremove-method"></a>Método SWbemQualifierSet. Remove

O método **Remove** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) exclui um qualificador nomeado da coleção.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do qualificador a ser removido.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

O parâmetro *iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O qualificador especificado não existe.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

A remoção deste qualificador é inválida.

</dd> </dl>

## <a name="remarks"></a>Comentários

Não é possível iterar uma coleção durante a remoção de itens porque, quando você remove um elemento de uma coleção, o ponteiro da coleção é movido para o próximo elemento. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemQualifierSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet. Add**](swbemqualifierset-add.md)
</dt> </dl>

 

 




