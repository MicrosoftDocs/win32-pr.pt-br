---
description: Cancela o registro do provedor associado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Método ITipAutocompleteClient:: unaconselheprovider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828740"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>Método ITipAutocompleteClient:: unaconselheprovider

Cancela o registro do provedor associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndfield* \[ no\]
</dt> <dd>

Identificador de janela do campo que fornece o recurso de preenchimento automático.

</dd> <dt>

*pIACProvider* \[ no\]
</dt> <dd>

Ponteiro de interface para o cancelamento do registro da interface do provedor de preenchimento automático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| parâmetro<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




