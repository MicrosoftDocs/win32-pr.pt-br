---
title: Interface IMsRdpClientAdvancedSettings2
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295823"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>Interface IMsRdpClientAdvancedSettings2

Gerencia configurações avançadas do cliente. Deriva da interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) . Essa interface inclui métodos para recuperar e definir propriedades avançadas (opcionais) para o controle ActiveX Área de Trabalho Remota.

Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings2 de IID** para **QueryInterface**.

## <a name="members"></a>Membros

A interface **IMsRdpClientAdvancedSettings2** herda de [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientAdvancedSettings2** tem essas propriedades.



| Propriedade                                                                                      | Tipo de acesso           | Descrição                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutoReconnect**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Somente leitura<br/>  | Especifica se o controle de cliente é capaz de se reconectar automaticamente à sessão atual no caso de uma desconexão de rede.<br/>    |
| [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Leitura/gravação<br/> | Especifica se o controle de cliente deve ser habilitado para se reconectar automaticamente a uma sessão no caso de uma desconexão de rede.<br/>            |
| [**MaxReconnectAttempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Leitura/gravação<br/> | Especifica o número de vezes para tentar se reconectar durante a reconexão automática. Os valores válidos dessa propriedade são de 0 a 200, inclusive.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 é definido como 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

