---
title: Propriedade IMsRdpClientAdvancedSettings7 SuperPanAccelerationFactor
description: Especifica ou recupera um valor que indica o fator de aceleração SuperPan. O fator de aceleração SuperPan determina a velocidade da tela no modo SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SuperPanAccelerationFactor
- Propriedade SuperPanAccelerationFactor Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade SuperPanAccelerationFactor
- Propriedade SuperPanAccelerationFactor Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919208"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>Propriedade IMsRdpClientAdvancedSettings7:: SuperPanAccelerationFactor

Especifica ou recupera um valor que indica o fator de aceleração SuperPan. O fator de aceleração SuperPan determina a velocidade da tela no modo SuperPan. O fator de aceleração é o número de pixels que a exibição de tela rola em uma determinada direção para cada pixel de movimento do mouse pelo cliente.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Valor da propriedade

O fator de aceleração SuperPan a ser definido. O fator de aceleração SuperPan é o número de pixels que a exibição de tela rola em uma determinada direção para cada pixel de movimento do mouse.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre SuperPan, consulte [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





