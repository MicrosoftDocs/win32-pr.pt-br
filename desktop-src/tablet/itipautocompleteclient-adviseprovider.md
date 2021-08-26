---
description: Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Método ITipAutocompleteClient:: Aconselheprovider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dd48cdfbf35c5132b42f8185cdc93f53ec34c77df78a51d16da9fa5a5311c144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938576"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>Método ITipAutocompleteClient:: Aconselheprovider

Registra o provedor com o cliente para permitir que o cliente chame o objeto de provedor de preenchimento automático do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndfield* \[ no\]
</dt> <dd>

O identificador de janela do campo que fornece o recurso de preenchimento automático.

</dd> <dt>

*pIACProvider* \[ no\]
</dt> <dd>

O ponteiro de interface para a interface de provedor de preenchimento automático.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete. h (também requer PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Método ITipAutocompleteClient:: unaconselheprovider**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




