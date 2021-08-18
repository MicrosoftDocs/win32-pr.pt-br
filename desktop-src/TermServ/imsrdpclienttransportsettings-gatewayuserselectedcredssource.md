---
title: Propriedade IMsRdpClientTransportSettings GatewayUserSelectedCredsSource
description: Define ou recupera a fonte de credencial Área de Trabalho Remota Gateway de RD (Gateway de RD) especificada pelo usuário.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Propriedade GatewayUserSelectedCredsSource Serviços de Área de Trabalho Remota
- Propriedade GatewayUserSelectedCredsSource Serviços de Área de Trabalho Remota , interface IMsRdpClientTransportSettings
- Interface IMsRdpClientTransportSettings Serviços de Área de Trabalho Remota , propriedade GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7632609f34d0133f37af4e8df16ebd574b3ef84e248c2bb3d2b1a84313957b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001006"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a>Propriedade IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource

Define ou recupera a fonte de credencial Área de Trabalho Remota Gateway de RD (Gateway de RD) especificada pelo usuário.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor da propriedade

Uma **variável ULONG** que especifica o método de autenticação do Gateway de RD. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ MODO \_ CREDS DE PROXY \_ \_ USERPASS** (0 (0x0))


</dt> <dd>

Use uma senha (NTLM) como o método de autenticação para o Gateway de RD.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ SMARTCARD** (1 (0x1))


</dt> <dd>

Use um cartão inteligente como o método de autenticação para o Gateway de RD.

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ PROXY \_ CREDS \_ MODE \_ ANY** (4 (0x4))


</dt> <dd>

Use qualquer método de autenticação para o Gateway de RD.

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





