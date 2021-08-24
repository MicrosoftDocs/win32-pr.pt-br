---
description: O método Item do objeto SWbemPropertySet obtém um SWbemProperty nomeado da coleção. Esse é o método padrão para este objeto .
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Método SWbemPropertySet.Item (Wbemdisp.h)
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
ms.openlocfilehash: afd0aede44effb14005f111429e365e6831df0d2cae8d1d0685539620c696723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897955"
---
# <a name="swbempropertysetitem-method"></a>Método SWbemPropertySet.Item

O **método Item** do objeto [**SWbemPropertySet**](swbempropertyset.md) obtém um [**SWbemProperty**](swbemproperty.md) nomeado da coleção. Esse é o método padrão para este objeto .

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ Em\]
</dt> <dd>

Obrigatórios. Nome da propriedade a ser recuperada.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. Esse valor deve ser zero se especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o [**objeto SWbemProperty**](swbemproperty.md) solicitado será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Item,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Falha não especificada.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749896
</dt> <dd>

Não há memória suficiente para que esse método seja executado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



 

 




