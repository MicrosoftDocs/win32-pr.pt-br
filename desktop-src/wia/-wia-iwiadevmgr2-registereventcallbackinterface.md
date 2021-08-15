---
description: registra um aplicativo em execução para notificação de eventos de aquisição de Windows Image (WIA) 2,0.
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
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965635"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Método IWiaDevMgr2:: RegisterEventCallbackInterface

registra um aplicativo em execução para notificação de eventos de aquisição de Windows Image (WIA) 2,0.

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

Tipo: **GUID \* const**

Especifica um ponteiro para o identificador de evento para o qual o aplicativo está se registrando. Consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md) para identificadores de evento padrão.

</dd> <dt>

*pIWiaEventCallback* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Especifica um ponteiro para a interface [**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que o WIA 2,0 usa para enviar a notificação de eventos.

</dd> <dt>

*pEventObject* \[ fora\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Recebe o endereço de um ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
