---
title: Propriedade de configurações de IRemoteDesktopClient
description: Recupera o objeto de configurações para o cliente de contêiner de aplicativo protocolo RDP (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota propriedade de configurações
- Propriedade de configurações Serviços de Área de Trabalho Remota, interface IRemoteDesktopClient
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClient, propriedade Settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918733"
---
# <a name="iremotedesktopclientsettings-property"></a>Propriedade IRemoteDesktopClient:: Settings

Recupera o objeto de configurações para o cliente de contêiner de aplicativo protocolo RDP (RDP).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto de configurações para o cliente RDP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IRemoteDesktopClient é definido como 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

