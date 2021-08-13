---
title: Propriedade EnableMouse de IMsRdpClientAdvancedSettings
description: Não há suporte a esta propriedade. | Propriedade EnableMouse de IMsRdpClientAdvancedSettings
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- Propriedade EnableMouse Serviços de Área de Trabalho Remota
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings
- Interface IMsRdpClientAdvancedSettings Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings2
- Interface IMsRdpClientAdvancedSettings2 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings3
- Interface IMsRdpClientAdvancedSettings3 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings4
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade EnableMouse
- A propriedade EnableMouse Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade EnableMouse
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb61f7763f92c46a80a7e0e45c5c476f4d3b64e7cbb735ba1e254641d90dae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608694"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a>Propriedade IMsRdpClientAdvancedSettings::EnableMouse

Não há suporte a esta propriedade.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a>Valor da propriedade

De definir esse parâmetro como 0 para desabilitar o recurso ou um valor não zero para habilitar o recurso.

## <a name="error-codes"></a>Códigos do Erro

Retorna **S \_ FALSE.**

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                       |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                                       |
| Fim do suporte ao servidor<br/>    | Nenhum compatível<br/>                                                                       |
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

 

 





