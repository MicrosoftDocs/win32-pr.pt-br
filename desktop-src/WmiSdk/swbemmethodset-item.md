---
description: O método Item do objeto SWbemMethodSet retorna um objeto SWbemMethod nomeado da coleção.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Método SWbemMethodSet.Item (Wbemdisp.h)
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
ms.openlocfilehash: fd78277be4611507a7f7a488dae0d4edda832afeac8c4a947d4c56277d9af397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679446"
---
# <a name="swbemmethodsetitem-method"></a>Método SWbemMethodSet.Item

O **método Item** do objeto [**SWbemMethodSet**](swbemmethodset.md) retorna um objeto [**SWbemMethod**](swbemmethod.md) nomeado da coleção.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ Em\]
</dt> <dd>

Obrigatórios. Nome do método a ser recuperado.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o [**objeto SWbemMethod**](swbemmethod.md) solicitado retornará.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Item,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

O *parâmetro iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** – 2147749894
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O método especificado não existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




