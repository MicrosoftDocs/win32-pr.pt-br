---
description: 'O método IWiaDevMgr2:: RegisterEventCallbackProgram registra um aplicativo para receber eventos de dispositivo. ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA (Windows Image Acquisition) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'Método IWiaDevMgr2:: RegisterEventCallbackProgram (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ebc99e61bf038c8db2ea537a1f8a5933ad512d21ec05cf51f6f8b7af5ede2b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441294"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>Método IWiaDevMgr2:: RegisterEventCallbackProgram

O método **IWiaDevMgr2:: RegisterEventCallbackProgram** registra um aplicativo para receber eventos de dispositivo. ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Os sinalizadores de registro. Pode ser definido com os valores a seguir.



| Valor                                                                                                                                                                                                           | Significado                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**\_retorno de \_ chamada de evento de registro WIA \_**</dt> </dl>       | Registre-se no evento.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**retorno de chamada do evento WIA \_ Cancelar registro \_ \_**</dt> </dl> | Exclua o registro do evento.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**\_ \_ manipulador padrão de Set WIA \_**</dt> </dl>                   | Defina o aplicativo como o manipulador de eventos padrão.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Um identificador de dispositivo. Passe **NULL** para registrar o evento em todos os dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ no\]
</dt> <dd>

Tipo: **GUID \* const**

O evento para o qual o aplicativo está se registrando. Para obter uma lista de GUIDs de eventos válidos, consulte [identificadores de evento WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

*bstrFullAppName* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O nome do caminho completo do aplicativo.

</dd> <dt>

*bstrCommandlineArg* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Os argumentos de linha de comando apropriados para o aplicativo.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O nome do aplicativo. O nome é exibido para o usuário quando vários aplicativos são registrados para o mesmo evento.

</dd> <dt>

*bstrDescription* \[ no\]
</dt> <dd>

Tipo: **BSTR**

A descrição do aplicativo. A descrição é exibida para o usuário quando vários aplicativos são registrados para o mesmo evento.

</dd> <dt>

*bstrIcon* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O ícone que representa o aplicativo. O ícone é exibido para o usuário quando vários aplicativos são registrados para o mesmo evento. A cadeia de caracteres contém o nome do aplicativo e o índice de base zero do ícone separado por uma vírgula, por exemplo, "MyApp, 0". Pode haver mais de um ícone que representa um aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use **IWiaDevMgr2:: RegisterEventCallbackProgram** para se registrar em eventos de dispositivo de hardware. Quando um evento ocorre quando um aplicativo é registrado para o, o aplicativo é iniciado e as informações do evento são transmitidas para o aplicativo.

Use o método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para recuperar um ponteiro para um objeto enumerador para propriedades de registro de evento.

Use apenas o método **IWiaDevMgr2:: RegisterEventCallbackProgram** para compatibilidade com versões anteriores com aplicativos não escritos para a arquitetura WIA 2,0. Use as interfaces de Component Object Model (COM) fornecidas pela arquitetura WIA 2,0 para novos aplicativos. Especificamente, chame [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) ou [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) para registrar um novo aplicativo para eventos de dispositivo.

Normalmente, esse método é chamado por um programa de instalação ou um script. O programa ou script de instalação registra o aplicativo para receber eventos de dispositivo WIA 2,0. Quando o evento ocorre, o aplicativo é iniciado pelo sistema de tempo de execução WIA 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




