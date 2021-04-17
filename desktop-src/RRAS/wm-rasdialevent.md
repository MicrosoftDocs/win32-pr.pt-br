---
title: Mensagem de WM_RASDIALEVENT (RAS. h)
description: O sistema operacional envia uma \_ mensagem do WM RASDIALEVENT para um procedimento de janela quando uma alteração de evento de estado ocorre durante um processo de conexão RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS de mensagens WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782291"
---
# <a name="wm_rasdialevent-message"></a>Mensagem do WM \_ RASDIALEVENT

O sistema operacional envia uma mensagem do **WM \_ RASDIALEVENT** para um procedimento de janela quando uma alteração de evento de estado ocorre durante um processo de conexão RAS. Isso acontece quando uma janela é especificada para manipular notificações de tais eventos usando o parâmetro de *notificador* de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Os dois parâmetros de mensagem são equivalentes aos parâmetros dos mesmos nomes que são usados com as funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valor de *wParam*. Equivalente ao parâmetro *RASCONNSTATE* das funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Especifica um valor de enumerador [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) que indica o estado que o processo de conexão de acesso remoto de RasDial está prestes a entrar.

</dd> <dt>

*dwError* 
</dt> <dd>

Valor de *lParam*. Equivalente ao parâmetro *dwError* das funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Um valor diferente de zero indica o erro que ocorreu ou zero se nenhum erro ocorreu.

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envia essa mensagem com *dwError* definido como zero na entrada para cada Estado de conexão. Se ocorrer um erro dentro de um estado, a mensagem será enviada novamente para o estado, desta vez com um valor *dwError* diferente de zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do serviço de acesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Mensagens do serviço de acesso remoto](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

