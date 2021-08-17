---
title: Propriedade RelativeMouseMode IMsRdpClientAdvancedSettings6
description: Especifica se o mouse deve usar o modo relativo.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota
- A propriedade RelativeMouseMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade RelativeMouseMode
- A propriedade RelativeMouseMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade RelativeMouseMode
- A propriedade RelativeMouseMode Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade RelativeMouseMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfe0551cf02f94f3494fde5ebf49ffb60c2bd4a966db1efb5f0dfeb3bd9e4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138809"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>Propriedade IMsRdpClientAdvancedSettings6::RelativeMouseMode

Especifica se o mouse deve usar o modo relativo. Conterá **VARIANT \_ TRUE** se o mouse estiver no modo relativo ou **VARIANT \_ FALSE** se o mouse estiver no modo absoluto.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a>Valor da propriedade

Contém o novo valor da propriedade.

## <a name="remarks"></a>Comentários

O modo do mouse indica como o controle ActiveX calcula as coordenadas do mouse que ele envia para o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Quando o mouse está no modo relativo, ActiveX controle calcula as coordenadas do mouse em relação à última posição do mouse. Quando o mouse está no modo absoluto, o controle ActiveX calcula as coordenadas do mouse em relação à área de trabalho do Host da Sessão RD servidor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista com SP1<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | \_IMs IIDRdpClientAdvancedSettings6 é definido como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





