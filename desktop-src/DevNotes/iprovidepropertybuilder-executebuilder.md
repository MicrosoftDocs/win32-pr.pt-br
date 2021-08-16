---
description: Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: Método IProvidePropertyBuilder::ExecuteBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 9aef31629cac755d5689de929c02fbc8d9b816bf868a48bd59df3d08c911d9b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827172"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Método IProvidePropertyBuilder::ExecuteBuilder

Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.

## <a name="syntax"></a>Sintaxe


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dispid* \[ Em\]
</dt> <dd>

O DISPID da propriedade para a qual o construtor exibe.

</dd> <dt>

*bstrGuidBldr* \[ Em\]
</dt> <dd>

O **BSTR** do GUID do construtor a ser invocado. Isso é retornado de [**MapToPropertyBuilder.**](iprovidepropertybuilder-mappropertytobuilder.md)

</dd> <dt>

*pdispApp* \[ Em\]
</dt> <dd>

Definido como **NULL.**

</dd> <dt>

*hwndBldrOwner* \[ Em\]
</dt> <dd>

Um alça para a janela pai do construtor pop-up.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

O valor atual da propriedade. Esse valor poderá ser modificado pelo objeto e será alterado para o novo valor se *pbActionCommitted* for **TRUE.**

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Um valor que indica se o construtor realizou uma ação no objeto . Pode ser usado quando um usuário modifica algo e, em seguida, pressiona OK na caixa de diálogo do construtor pop-up.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




