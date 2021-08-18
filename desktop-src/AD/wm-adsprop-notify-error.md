---
title: WM_ADSPROP_NOTIFY_ERROR mensagem (Adsprop.h)
description: A mensagem WM ADSPROP NOTIFY ERROR adiciona uma mensagem de erro a uma lista de mensagens de erro exibidas chamando \_ \_ a função \_ ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_ERROR mensagem do Active Directory
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
ms.openlocfilehash: 52f88cd4c60dcfcceed60ca644f7c59f65bee16e344cc17664e8b4be1ee18fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024284"
---
# <a name="wm_adsprop_notify_error-message"></a>Mensagem DE ERRO WM \_ ADSPROP \_ NOTIFY \_

A **mensagem WM \_ ADSPROP NOTIFY \_ \_ ERROR** adiciona uma mensagem de erro a uma lista de mensagens de erro exibidas chamando a [**função ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador do objeto de notificação. Esse é o *parâmetro hNotifyObject* obtido por [**ADsPropCreateNotifyObj.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

</dd> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) que contém dados de mensagem de erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

A [**função ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) é o método preferencial para enviar essa mensagem.

As mensagens de erro adicionadas pela **mensagem WM \_ ADSPROP NOTIFY \_ \_ ERROR** são acumuladas até [**que ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) seja chamado. **ADsPropShowErrorDialog** combina e exibe as mensagens de erro acumuladas. Quando a caixa de diálogo de erro é descartada, as mensagens de erro acumuladas são excluídas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



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

 

 





