---
description: Registra um aplicativo em execução para notificação de eventos de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'Método IWiaDevMgr2:: RegisterEventCallbackInterface (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169537"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Método IWiaDevMgr2:: RegisterEventCallbackInterface

Registra um aplicativo em execução para notificação de eventos de aquisição de imagem do Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o identificador exclusivo de um dispositivo WIA 2,0. Defina esse parâmetro como **NULL** para registrar o evento em todos os dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ no\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica um ponteiro para o identificador de evento para o qual o aplicativo está se registrando. Consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md) para identificadores de evento padrão.

</dd> <dt>

_pIWiaEventCallback * \[ in\]
</dt> <dd>

Tipo: **[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

Especifica um ponteiro para a interface [_ *IWiaEventCallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que o WIA 2,0 usa para enviar a notificação de eventos.

</dd> <dt>

*pEventObject* \[ fora\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Recebe o endereço de um ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Retorna os códigos de erro COM padrão ou o seguinte.



| Código de retorno                                                                               | Descrição                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | A interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) não pode ser retornada. <br/> |



 

## <a name="remarks"></a>Comentários

> [!WARNING]
> O uso dos métodos [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** e [**DeviceManager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) do mesmo processo após a reinicialização do serviço de imagem ainda pode causar uma violação de acesso, se as funções tiverem sido usadas antes de o serviço ser interrompido.

 

Quando os aplicativos WIA 2,0 começam a ser executados, eles usam esse método para se registrar para receber eventos de dispositivo de hardware. Isso impede que o aplicativo seja reiniciado quando outro evento para o qual ele está registrado ocorre. Quando um aplicativo chama **IWiaDevMgr2:: RegisterEventCallbackInterface** para se registrar para receber eventos WIA 2,0 de um dispositivo, os eventos registrados são roteados para o programa pela WIA 2,0.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *pEventObject* .

> [!Note]  
> Em um aplicativo multithread, o retorno de chamada de notificação de evento pode vir em um thread diferente daquele que registrou o retorno de chamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
