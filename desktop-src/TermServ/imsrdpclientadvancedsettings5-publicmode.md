---
title: Propriedade IMsRdpClientAdvancedSettings5 Públicomode
description: Define ou recupera a configuração para o modo público. O modo público impede que o cliente Caching os dados do usuário para o sistema local.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade públicomode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings5, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings6, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings7, Propriedade Publicmode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings8, Propriedade Publicmode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755162"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a>IMsRdpClientAdvancedSettings5: Propriedade ublicMode de:P

Define ou recupera a configuração para o modo público. O modo público impede que o cliente Caching os dados do usuário para o sistema local.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a>Valor da propriedade

Define a configuração de modo público como **Variant \_ true** ou **Variant \_ false**. Se definido como **Variant \_ true**, a configuração de modo público será habilitada.

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

 

 





