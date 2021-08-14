---
title: Propriedade LoadBalanceInfo de IMsRdpClientAdvancedSettings
description: Especifica o cookie de balanceamento de carga que será colocado no pacote solicitação de conexão X.224 na sequência de conexão de protocolo Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) do servidor.
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings
- Interface IMsRdpClientAdvancedSettings Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings2
- Interface IMsRdpClientAdvancedSettings2 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings3
- Interface IMsRdpClientAdvancedSettings3 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings4
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
- A propriedade LoadBalanceInfo Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe7ca9b9ed68f3327779177e706ee5a943c9e6580e2b789e2b96e74ee9f0b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353035"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a>Propriedade IMsRdpClientAdvancedSettings::LoadBalanceInfo

Especifica o cookie de balanceamento de carga que será colocado no pacote solicitação de conexão X.224 na sequência de conexão de protocolo Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) do servidor.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a>Valor da propriedade

Ponteiro para o novo cookie. Para obter mais informações, consulte a seção de comentários.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

As informações de balanceamento de carga são usadas pelos roteadores de balanceamento de carga para escolher o melhor servidor para o cliente ao usar farms de Host da Sessão RD servidores. O Host da Sessão RD servidor em si não usa essas informações e as descartará.

O cookie usa a seguinte sintaxe, que faz a resiência de minúsculas:

**Cookie: msts=**_IpAddressAndPortNumber_*_\\ r \\ n_*

Em *que IpAddressAndPortNumber* é o endereço IP e o número da porta, em ordem de byte de rede.

Por exemplo, o cookie usado para acessar o endereço IP de 172.31.249.216, número da porta 3389 é o seguinte:

**Cookie: msts=3640205228.15629.0000 \\ r \\ n**

Os quatro zeros finais são opcionais e reservados. O ponto decimal final é necessário, assim como o retorno de carro à direita e a linha de linha. O comprimento da cadeia de caracteres, em caracteres, deve ser um múltiplo de 2, portanto, adicione um espaço, se necessário.

Se nenhum cookie for fornecido, o padrão será **Cookie: mstshash=**_UserName_*_\\ r \\ n_*.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | \_IMs IIDRdpClientAdvancedSettings é definido como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





