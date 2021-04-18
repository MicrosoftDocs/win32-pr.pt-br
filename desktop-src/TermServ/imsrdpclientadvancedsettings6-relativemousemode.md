---
title: Propriedade IMsRdpClientAdvancedSettings6 RelativeMouseMode
description: Especifica se o mouse deve usar o modo relativo.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade RelativeMouseMode
- Propriedade RelativeMouseMode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade RelativeMouseMode
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
ms.openlocfilehash: 31c575acefbfef54dc4c858f465f0cdde2ce8bc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757190"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>Propriedade IMsRdpClientAdvancedSettings6:: RelativeMouseMode

Especifica se o mouse deve usar o modo relativo. Contém **Variant \_ true** se o mouse estiver no modo relativo ou **Variant \_ false** se o mouse estiver no modo absoluto.

Esta propriedade é de leitura/gravação.

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

O modo de mouse indica como o controle ActiveX calcula as coordenadas do mouse que ele envia para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Quando o mouse está no modo relativo, o controle ActiveX calcula as coordenadas do mouse em relação à última posição do mouse. Quando o mouse estiver no modo absoluto, o controle ActiveX calculará as coordenadas do mouse relativas à área de trabalho do servidor de Host da Sessão RD.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista com SP1<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





