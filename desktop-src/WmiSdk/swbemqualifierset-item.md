---
description: O método Item do objeto SWbemQualifierSet retorna um objeto SWbemQualifier nomeado da coleção. Esse é o método padrão desse objeto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Método SWbemQualifierSet.Item (Wbemdisp.h)
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
ms.openlocfilehash: 99b735f52ac4d311af6e35f7e214322c55345e4c029e73a342baa52dfa72de6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312987"
---
# <a name="swbemqualifiersetitem-method"></a>Método SWbemQualifierSet.Item

O **método Item** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) retorna um objeto [**SWbemQualifier**](swbemqualifier.md) nomeado da coleção. Esse é o método padrão desse objeto.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ Em\]
</dt> <dd>

Obrigatórios. Nome do qualificador a ser recuperado.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o [**objeto SWbemQualifier**](swbemqualifier.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Item,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

O *parâmetro iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O qualificador especificado não existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




