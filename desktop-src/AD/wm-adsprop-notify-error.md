---
title: Mensagem de WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: A mensagem de erro de notificação do WM \_ ADSPROP \_ \_ adiciona uma mensagem de erro a uma lista de mensagens de erro que são exibidas chamando a função ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085593"
---
# <a name="wm_adsprop_notify_error-message"></a>\_Mensagem de \_ erro de notificação do WM ADSPROP \_

A mensagem de **erro de notificação do WM \_ \_ \_ ADSPROP** adiciona uma mensagem de erro a uma lista de mensagens de erro que são exibidas chamando a função [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Identificador do objeto de notificação. Esse é o parâmetro *hNotifyObject* obtido por [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) que contém dados de mensagem de erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

A função [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) é o método preferencial para enviar essa mensagem.

As mensagens de erro adicionadas pela mensagem de **erro de notificação do WM \_ \_ \_ ADSPROP** são acumuladas até que [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) seja chamado. **ADsPropShowErrorDialog** combina e exibe as mensagens de erro acumuladas. Quando a caixa de diálogo de erro é ignorada, as mensagens de erro acumuladas são excluídas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens em Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





