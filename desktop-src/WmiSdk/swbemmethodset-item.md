---
description: O método item do objeto SWbemMethodSet retorna um objeto nomeado SWbemMethod da coleção.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Método SWbemMethodSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813543"
---
# <a name="swbemmethodsetitem-method"></a>Método SWbemMethodSet. Item

O método **Item** do objeto [**SWbemMethodSet**](swbemmethodset.md) retorna um objeto nomeado [**SWbemMethod**](swbemmethod.md) da coleção.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do método a recuperar.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o objeto [**SWbemMethod**](swbemmethod.md) solicitado retornará.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

O parâmetro *iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** -2147749894
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O método especificado não existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHODSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemMethodSet de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




