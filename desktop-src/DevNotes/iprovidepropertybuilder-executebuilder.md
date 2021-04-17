---
description: Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Método IProvidePropertyBuilder:: ExecuteBuilder'
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
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749929"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Método IProvidePropertyBuilder:: ExecuteBuilder

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

*DISPID* \[ no\]
</dt> <dd>

O DISPID da propriedade para a qual o Construtor exibe.

</dd> <dt>

*bstrGuidBldr* \[ no\]
</dt> <dd>

O **BSTR** do GUID do Construtor a ser invocado. Isso é retornado de [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).

</dd> <dt>

*pdispApp* \[ no\]
</dt> <dd>

Defina como **nulo**.

</dd> <dt>

*hwndBldrOwner* \[ no\]
</dt> <dd>

Um identificador para a janela do construtor pop-up pai.

</dd> <dt>

*pvarValue* \[ entrada, saída\]
</dt> <dd>

O valor atual da propriedade. Esse valor pode ser modificado pelo objeto e alterado para o novo valor se *pbActionCommitted* for **true**.

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Um valor que indica se o Construtor executou uma ação no objeto. Pode ser usado quando um usuário modifica algo e, em seguida, pressiona OK na caixa de diálogo Construtor de pop-ups.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




