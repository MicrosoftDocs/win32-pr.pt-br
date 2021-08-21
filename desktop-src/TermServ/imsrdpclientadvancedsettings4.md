---
title: Interface IMsRdpClientAdvancedSettings4
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota
- Interface IMsRdpClientAdvancedSettings4 Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aaf0e09131264440fc1efaaad3291e110ea718312b042b232837cdff4722494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855304"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a>Interface IMsRdpClientAdvancedSettings4

Gerencia configurações avançadas do cliente. Deriva da interface [**IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md) Essa interface inclui métodos para recuperar e definir propriedades avançadas (opcionais) para o Área de Trabalho Remota ActiveX controle.

Para obter uma instância dessa interface, use a propriedade [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMs IIDRdpClientAdvancedSettings4** para **QueryInterface**.

## <a name="members"></a>Membros

A interface **IMsRdpClientAdvancedSettings4** herda de [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md). **IMsRdpClientAdvancedSettings4** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientAdvancedSettings4** tem essas propriedades.



| Propriedade                                                                                    | Tipo de acesso           | Descrição                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [**Authenticationlevel**](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | Leitura/gravação<br/> | Especifica o nível de autenticação a ser usado para a conexão.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2008 com SP1<br/>                                     |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings4 é definido como FBA7F64E-7345-4405-AE50-FA4A763DC0DE<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**Imstscadvancedsettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Conexão Web de Área de Trabalho Remota referência](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

