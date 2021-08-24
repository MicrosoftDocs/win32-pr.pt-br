---
description: Não registrou o provedor associado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: Método ITipAutocompleteClient::UnadviseProvider (TipAutoComplete.h)
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
ms.openlocfilehash: d4f573e1dab88e8556dc8c6011173cd3a2284a87d9f98ac6d05cea13cef65ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712096"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>Método ITipAutocompleteClient::UnadviseProvider

Não registrou o provedor associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWndField* \[ Em\]
</dt> <dd>

Alça de janela do campo que fornece o recurso de conclusão automática.

</dd> <dt>

*pIACProvider* \[ Em\]
</dt> <dd>

Ponteiro de interface para a interface de provedor de conclusão automática a ser não contada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>TipAutoComplete.h (também requer Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITipAutocompleteClient Interface**](itipautocompleteclient.md)
</dt> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




