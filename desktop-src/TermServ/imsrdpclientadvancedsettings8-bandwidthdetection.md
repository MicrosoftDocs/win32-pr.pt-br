---
title: Propriedade IMsRdpClientAdvancedSettings8 BandwidthDetection
description: Especifica se as alterações de largura de banda são detectadas automaticamente.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade BandwidthDetection
- Propriedade BandwidthDetection Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760128"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a>Propriedade IMsRdpClientAdvancedSettings8:: BandwidthDetection

Especifica se as alterações de largura de banda são detectadas automaticamente.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a>Valor da propriedade

**Variante \_ TRUE** se as alterações de largura de banda forem detectadas automaticamente ou **Variant \_ false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





