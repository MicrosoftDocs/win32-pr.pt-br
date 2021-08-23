---
title: Propriedade IMsTscAdvancedSettings ContainerHandledFullScreen
description: Especifica se o modo de tela inteira manipulado por contêiner está habilitado.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, propriedade ContainerHandledFullScreen
- Propriedade ContainerHandledFullScreen Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, propriedade ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975581aaca4aad2511396e8ec426a7bf2a4720ff54202d42fbe932c0c2e9464d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513116"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>Propriedade IMsTscAdvancedSettings:: ContainerHandledFullScreen

Especifica se o modo de tela inteira manipulado por contêiner está habilitado.

> [!Note]  
> o valor da propriedade **ContainerHandledFullScreen** não tem efeito quando o controle de ActiveX de Área de Trabalho Remota é seguro para script e retorna **S \_ FALSE** quando é feita uma tentativa de alterar o valor.

 

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Valor da propriedade

Defina esse parâmetro como **true** para habilitar o modo ou outro valor para desabilitar o modo.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido. Retornará **S \_ false** se não houver suporte.

## <a name="remarks"></a>Comentários

Quando esse modo está habilitado, o contêiner atual processa o comutador para dentro e para fora do modo de tela inteira. Esse método deve ser usado somente se o contêiner atual precisar de controle extensivo sobre o comportamento do modo de tela inteira. Quando essa propriedade é definida, o controle não entra nem sai do modo de tela inteira em resposta à combinação de teclas de atalho do modo de tela inteira (CTRL + ALT + BREAK); em vez disso, os eventos [**IMsTscAxEvents:: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) e [**IMsTscAxEvents:: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) são chamados. Consulte [**IMsTscAxEvents**](imstscaxevents-interface.md) para obter mais informações sobre esses eventos.

A maioria dos aplicativos de contêiner não precisará usar o modo de tela inteira manipulado por contêiner.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





