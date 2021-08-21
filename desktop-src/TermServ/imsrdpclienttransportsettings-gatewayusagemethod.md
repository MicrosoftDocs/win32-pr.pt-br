---
title: Propriedade IMsRdpClientTransportSettings GatewayUsageMethod
description: Especifica quando usar um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayUsageMethod
- Propriedade GatewayUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a177d191d3303cf44778713ebdef88db955d28ede58691bda1e9ad05aa51a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001036"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>Propriedade IMsRdpClientTransportSettings:: GatewayUsageMethod

Especifica quando usar um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **ULONG** que especifica o método de uso do servidor de gateway de área de trabalho remota. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modo proxy \_ nenhum \_ direto** (0 (0x0))


</dt> <dd>

Não use um servidor de gateway de área de trabalho remota. Na interface do usuário do cliente do Conexão de Área de Trabalho Remota (RDC), a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está desmarcada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modo proxy \_ direto** (1 (0x1))


</dt> <dd>

Sempre use um servidor de gateway de área de trabalho remota. Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está desmarcada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Detecção de modo proxy** (2 (0x2))


</dt> <dd>

Use um servidor de gateway de área de trabalho remota se não for possível estabelecer uma conexão direta com o servidor de Host da Sessão RD. Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está marcada.

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Padrão de modo proxy** (3 (0x3))


</dt> <dd>

Use as configurações padrão do servidor Gateway RD.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_Modo proxy \_ None \_ detectar** (4 (0x4))


</dt> <dd>

Não use um servidor de gateway de área de trabalho remota. Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está marcada.

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

 

 





