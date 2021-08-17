---
title: Propriedade IMsRdpClientAdvancedSettings7 EnableSuperPan
description: Especifica ou recupera um valor booliano que indica se SuperPan está habilitado ou desabilitado.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EnableSuperPan
- Propriedade EnableSuperPan Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade EnableSuperPan
- Propriedade EnableSuperPan Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd48fbb42f65e42b0cdeee3560c93361c49283eecfa4ee3a792a19f6081b07b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757334"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>Propriedade IMsRdpClientAdvancedSettings7:: EnableSuperPan

Especifica ou recupera um valor booliano que indica se SuperPan está habilitado ou desabilitado. SuperPan é um recurso que permite que um usuário navegue facilmente por uma área de trabalho remota no modo de tela inteira, quando as dimensões da área de trabalho remota são maiores do que as dimensões da janela do cliente atual. Em vez de usar barras de rolagem para navegar na área de trabalho, o usuário pode apontar para a borda da janela e a área de trabalho remota será rolada automaticamente nessa direção. SuperPan não dá suporte a mais de um monitor.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Valor da propriedade

Um **valor \_ bool de variante** que especifica se SuperPan está habilitado. Um valor de **Variant \_ true** especifica que SuperPan está habilitado.

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
</dt> </dl>

 

 





