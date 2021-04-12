---
title: Propriedade IMsRdpClientTransportSettings GatewayProfileUsageMethod
description: Especifica se as configurações padrão de gateway de Área de Trabalho Remota (Gateway RD) devem ser usadas.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayProfileUsageMethod
- Propriedade GatewayProfileUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369579"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a>Propriedade IMsRdpClientTransportSettings:: GatewayProfileUsageMethod

Especifica se as configurações padrão de gateway de Área de Trabalho Remota (Gateway RD) devem ser usadas.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a>Valor da propriedade

O método de uso de perfil de gateway de área de trabalho remota. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ Modo de perfil de PROXY \_ \_ \_ padrão** (0 (0x0))


</dt> <dd>

Use o modo de perfil padrão, conforme especificado pelo administrador.

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ Modo de perfil de PROXY \_ \_ \_ explícito** (1 (0x1))


</dt> <dd>

Use configurações explícitas, conforme especificado pelo usuário.

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

 

 





