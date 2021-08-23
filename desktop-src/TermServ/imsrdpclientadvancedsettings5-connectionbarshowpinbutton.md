---
title: Propriedade IMsRdpClientAdvancedSettings5 ConnectionBarShowPinButton
description: Define ou recupera a configuração do botão PIN na barra de conexão.
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade ConnectionBarShowPinButton
- Propriedade ConnectionBarShowPinButton Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ConnectionBarShowPinButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a978f6d1b6a26fe84f5ad590cfc41ab384d6ba49f1e265eecc0ea408b67b59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001384"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a>Propriedade IMsRdpClientAdvancedSettings5:: ConnectionBarShowPinButton

Define ou recupera a configuração do botão PIN na barra de conexão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano de **true** ou **false**. Um valor **true** mostra o botão PIN na barra de conexão. Um valor de **false** oculta o botão de PIN na barra de conexão.

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

 

 





