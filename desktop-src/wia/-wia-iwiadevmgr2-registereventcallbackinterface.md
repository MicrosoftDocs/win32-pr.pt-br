---
description: Registra um aplicativo em execução para Windows de evento WIA (Aquisição de Imagem) 2.0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: Método IWiaDevMgr2::RegisterEventCallbackInterface (Wia.h)
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
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>Método IWiaDevMgr2::RegisterEventCallbackInterface

Registra um aplicativo em execução para Windows de evento WIA (Aquisição de Imagem) 2.0.

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

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> <dt>

*bstrDeviceID* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o identificador exclusivo de um dispositivo WIA 2.0. De definir esse parâmetro como **NULL** para registrar o evento em todos os dispositivos WIA 2.0.

</dd> <dt>

*pEventGUID* \[ Em\]
</dt> <dd>

Tipo: **const \* GUID**

Especifica um ponteiro para o identificador de evento para o que o aplicativo está registrando. Consulte [Identificadores de evento WIA para](-wia-wia-event-identifiers.md) identificadores de evento padrão.

</dd> <dt>

*pIWiaEventCallback* \[ Em\]
</dt> <dd>

Tipo: **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Especifica um ponteiro para a interface [**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que o WIA 2.0 usa para enviar notificação de evento.

</dd> <dt>

*pEventObject* \[ out\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Recebe o endereço de um ponteiro para a interface [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Retorna os códigos de erro COM padrão ou o seguinte.



| Código de retorno                                                                               | Descrição                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | A [interface IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) não pode ser retornada. <br/> |



 

## <a name="remarks"></a>Comentários

> [!WARNING]
> Usar os métodos [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface** e [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) do mesmo processo depois que o Serviço de Imagem Ainda for reiniciado poderá causar uma violação de acesso, se as funções foram usadas antes que o serviço fosse interrompido.

 

Quando os aplicativos WIA 2.0 começam a ser executados, eles usam esse método para se registrar para receber eventos de dispositivo de hardware. Isso impede que o aplicativo seja reiniciado quando ocorre outro evento para o qual ele está registrado. Depois que um aplicativo chama **IWiaDevMgr2::RegisterEventCallbackInterface** para se registrar para receber eventos WIA 2.0 de um dispositivo, os eventos registrados são roteados para o programa pelo WIA 2.0.

Os aplicativos devem chamar [o método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface que recebem por meio do *parâmetro pEventObject.*

> [!Note]  
> Em um aplicativo multithread, o retorno de chamada de notificação de evento pode entrar em um thread diferente do que registrou o retorno de chamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
