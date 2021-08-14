---
title: Propriedade RedirectClipboard IMsRdpClientAdvancedSettings5
description: Define ou recupera a configuração para redirecionamento da área de transferência.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Propriedade RedirectClipboard Serviços de Área de Trabalho Remota
- A propriedade RedirectClipboard Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings5
- Interface IMsRdpClientAdvancedSettings5 Serviços de Área de Trabalho Remota , propriedade RedirectClipboard
- A propriedade RedirectClipboard Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade RedirectClipboard
- A propriedade RedirectClipboard Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade RedirectClipboard
- A propriedade RedirectClipboard Serviços de Área de Trabalho Remota , interface IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5847ef4ccb5798ea74cccecbcabbb04303df93f3cd9a8a6155cd94eabbc8a824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352280"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a>Propriedade IMsRdpClientAdvancedSettings5::RedirectClipboard

Define ou recupera a configuração para redirecionamento da área de transferência.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a>Valor da propriedade

Define o modo de redirecionamento da área de transferência **como TRUE** ou **FALSE.** Se definido como **TRUE,** o modo de redirecionamento da área de transferência será habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





