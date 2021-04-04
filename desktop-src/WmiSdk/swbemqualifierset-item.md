---
description: O método item do objeto SWbemQualifierSet retorna um objeto nomeado SWbemQualifier da coleção. Esse é o método padrão deste objeto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837166"
---
# <a name="swbemqualifiersetitem-method"></a>Método SWbemQualifierSet. Item

O método **Item** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) retorna um objeto nomeado [**SWbemQualifier**](swbemqualifier.md) da coleção. Esse é o método padrão deste objeto.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do qualificador a recuperar.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemQualifier**](swbemqualifier.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

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

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemQualifierSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




