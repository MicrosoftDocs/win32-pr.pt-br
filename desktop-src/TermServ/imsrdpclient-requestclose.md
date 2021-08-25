---
title: Método RequestClose IMsRdpClient
description: Solicita um desligamento normalmente do Área de Trabalho Remota ActiveX controle.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Método RequestClose Serviços de Área de Trabalho Remota
- O método RequestClose Serviços de Área de Trabalho Remota , interface IMsRdpClient
- Interface IMsRdpClient Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient2
- Interface IMsRdpClient2 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota , interface IMsRdpClient3
- Interface IMsRdpClient3 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , método RequestClose
- O método RequestClose Serviços de Área de Trabalho Remota interface , IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , método RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae812c27b0c280ca3a6cd879d5af86181de85793ec6092441fb83b45c74d8656
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010176"
---
# <a name="imsrdpclientrequestclose-method"></a>Método IMsRdpClient::RequestClose

Solicita um desligamento normalmente do Área de Trabalho Remota ActiveX controle. Um desligamento normalmente pode incluir o encerramento da sessão de Serviços de Área de Trabalho Remota do usuário, mas não desliga o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCloseStatus* \[ out\]
</dt> <dd>

Valor da [**enumeração ControlCloseStatus**](controlclosestatus.md) que indica se o aplicativo pode fechar o controle imediatamente. A seguir está uma lista de valores possíveis.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

O aplicativo de contêiner pode continuar a fechar o controle imediatamente. Esse valor também pode indicar que a conexão já foi encerrada.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

O aplicativo de contêiner não deve fechar o controle imediatamente; O aplicativo deve aguardar que um dos eventos descritos na seção Comentários a seguir ocorra antes de fechar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Se o *parâmetro pCloseStatus* for igual a **controlCloseWaitForEvents**, o aplicativo deverá aguardar que um dos seguintes eventos ocorra antes que o aplicativo feche o controle:

-   [**IMsTscAxEvents::OnDisconnected.**](imstscaxevents-ondisconnected.md) Se o usuário não estiver conectado à sessão Serviços de Área de Trabalho Remota, o aplicativo poderá chamar a [**função DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas as janelas e fechar o controle.
-   [**IMsTscAxEvents::OnConfirmClose.**](imstscaxevents-onconfirmclose.md) Se o usuário estiver conectado à sessão Serviços de Área de Trabalho Remota, o controle disparará um **evento OnConfirmClose.** Esse evento permite que o aplicativo solicita ao usuário se deve fechar a conexão. Se o usuário responder sim ao prompt, o aplicativo de contêiner poderá chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir todas as janelas e fechar o controle.

**RequestClose** permite que um aplicativo de contêiner solicite ao usuário se deve fechar uma conexão. Para obter mais informações, [**consulte IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient é definido como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imsrdpclient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

