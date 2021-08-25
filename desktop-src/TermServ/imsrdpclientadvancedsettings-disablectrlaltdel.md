---
title: Propriedade IMsRdpClientAdvancedSettings DisableCtrlAltDel
description: Especifica se a tela explicativa inicial no Winlogon deve ser exibida.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings
- Interface IMsRdpClientAdvancedSettings Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings2
- Interface IMsRdpClientAdvancedSettings2 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings3
- Interface IMsRdpClientAdvancedSettings3 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings4
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
- A propriedade DisableCtrlAltDel Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c524945afe4fbaaa0498f579641a32d3f55f37e88335be82e8fa308fae502f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871035"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a>Propriedade IMsRdpClientAdvancedSettings::D isableCtrlAltDel

Especifica se a tela explicativa inicial no Winlogon deve ser exibida.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a>Valor da propriedade

De definir esse parâmetro como 0 para desabilitar o recurso ou um valor não zero para habilitar o recurso.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

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

 

 





