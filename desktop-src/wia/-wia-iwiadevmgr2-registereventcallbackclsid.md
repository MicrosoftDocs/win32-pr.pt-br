---
description: 'O método IWiaDevMgr2:: RegisterEventCallbackCLSID registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'Método IWiaDevMgr2:: RegisterEventCallbackCLSID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9137fdd33f59eb841a54e84a6d12bb0b08968ac29c8737afbf56f66c57176c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965639"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>Método IWiaDevMgr2:: RegisterEventCallbackCLSID

O método **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica os sinalizadores de registro. Pode ser definido com os seguintes valores:



| Sinalizador de registro                | Significado                                           |
|----------------------------------|---------------------------------------------------|
| \_retorno de \_ chamada de evento de registro WIA \_   | Registre-se no evento.                           |
| retorno de chamada do evento WIA \_ Cancelar registro \_ \_ | Exclua o registro do evento.            |
| \_ \_ manipulador padrão de Set WIA \_       | Defina o aplicativo como o manipulador de eventos padrão. |



 

</dd> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica um identificador de dispositivo. Passe **NULL** para registrar o evento em todos os dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ no\]
</dt> <dd>

Tipo: **GUID \* const**

Especifica o evento para o qual o aplicativo está se registrando. Para obter uma lista de eventos padrão, consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

*pCLSID* \[ no\]
</dt> <dd>

Tipo: **GUID \* const**

Ponteiro para a ID de classe do aplicativo (**CLSID**). O sistema de tempo de execução WIA 2,0 usa o **CLSID** do aplicativo para iniciar o aplicativo quando ocorre um evento no qual ele está registrado.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome do aplicativo que se registra para o evento.

</dd> <dt>

*bstrDescription* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica uma descrição de texto do aplicativo que se registra para o evento.

</dd> <dt>

*bstrIcon* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o nome de um arquivo de imagem a ser usado para o ícone do aplicativo que se registra para o evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os aplicativos WIA 2,0 usam esse método para se registrar para receber eventos de dispositivo de hardware. Depois que **IWiaDevMgr2:: RegisterEventCallbackCLSID** for chamado, o aplicativo será registrado para receber eventos de dispositivo WIA 2,0, mesmo se ele não estiver em execução.

Quando o evento ocorre, o sistema WIA 2,0 determina qual aplicativo está registrado para receber o evento. Ele usa a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e o CLSID especificado no parâmetro *pCLSID* para criar uma instância do aplicativo e, em seguida, chama o método [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) para transmitir as informações do evento para o aplicativo.

Um aplicativo pode invocar o método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para enumerar informações de registro de evento.

Se o aplicativo não for um componente COM (Component Object Model registrado) e não for compatível com a arquitetura WIA 2,0, use o método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar um aplicativo para eventos de dispositivo.

> [!Note]  
> Em um aplicativo multi-threaded, não há nenhuma garantia de que o retorno de chamada de notificação de evento seja retornado no mesmo thread que registrou o retorno de chamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
