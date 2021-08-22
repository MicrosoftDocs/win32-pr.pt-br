---
title: Propriedade IMsRdpClientTransportSettings GatewayProfileUsageMethod
description: Especifica se as configurações padrão Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Propriedade GatewayProfileUsageMethod Serviços de Área de Trabalho Remota
- Propriedade GatewayProfileUsageMethod Serviços de Área de Trabalho Remota , interface IMsRdpClientTransportSettings
- Interface IMsRdpClientTransportSettings Serviços de Área de Trabalho Remota , propriedade GatewayProfileUsageMethod
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
ms.openlocfilehash: 3386e6a38c99539aebb84280dc8250b2d779f5d81229763d2d926ae499e144e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138619"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a>Propriedade IMsRdpClientTransportSettings::GatewayProfileUsageMethod

Especifica se as configurações padrão Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

Essa propriedade é leitura/gravação.

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

O método de uso do perfil do Gateway de RD. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ PADRÃO \_ DO MODO DE PERFIL \_ \_ DE PROXY** (0 (0x0))


</dt> <dd>

Use o modo de perfil padrão, conforme especificado pelo administrador.

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ MODO \_ DE PERFIL PROXY \_ \_ EXPLÍCITO** (1 (0x1))


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

 

 





