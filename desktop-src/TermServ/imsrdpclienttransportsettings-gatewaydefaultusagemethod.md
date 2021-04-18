---
title: Propriedade IMsRdpClientTransportSettings GatewayDefaultUsageMethod
description: O método de uso padrão para gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayDefaultUsageMethod
- Propriedade GatewayDefaultUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788035"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Propriedade IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod

O método de uso padrão para gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para o método de uso padrão para o Gateway RD. Retorna uma União das configurações de usuário definidas por [**Put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)e configurações de política de grupo. Se nenhuma configuração de usuário tiver sido definida por **Put \_ GatewayUsageMethod ()**, o **Get \_ GatewayDefaultUsageMethod ()** retornará o valor padrão da **\_ \_ \_ detecção do modo proxy de TSC**.

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

 

 





