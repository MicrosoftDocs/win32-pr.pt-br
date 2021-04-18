---
title: Interface IMsRdpClientAdvancedSettings6
description: Expõe as propriedades que gerenciam as configurações avançadas do controle ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings6, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761331"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>Interface IMsRdpClientAdvancedSettings6

Expõe as propriedades que gerenciam as configurações avançadas do controle ActiveX. A interface **IMsRdpClientAdvancedSettings6** é derivada da interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .

Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings6 de IID** para **QueryInterface**.

## <a name="members"></a>Membros

A interface **IMsRdpClientAdvancedSettings6** herda de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md). **IMsRdpClientAdvancedSettings6** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientAdvancedSettings6** tem essas propriedades.



| Propriedade                                                                                                  | Tipo de acesso           | Descrição                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | Leitura/gravação<br/> | Especifica o nome da entidade de serviço (SPN) a ser usado para autenticação no servidor.<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | Somente leitura<br/>  | Especifica o tipo de autenticação usado para essa conexão.<br/>                                                          |
| [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | Leitura/gravação<br/> | Recupera ou especifica se o controle ActiveX deve tentar se conectar ao servidor para fins administrativos.<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | Leitura/gravação<br/> | Especifica se o provedor de serviços de segurança de credencial (CredSSP) está habilitado para esta conexão.<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | Leitura/gravação<br/> | Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + seta para a esquerda.<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | Leitura/gravação<br/> | Especifica o código de chave virtual a ser adicionado a CTRL + ALT para determinar a substituição de tecla de atalho para CTRL + ALT + seta direita.<br/>         |
| [**PCB**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | Leitura/gravação<br/> | Especifica a configuração de BLOB de preconexão (PCB) a ser usada antes de se conectar para transmissão para o servidor.<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | Leitura/gravação<br/> | Especifica se o mouse deve usar o modo relativo.<br/>                                                                   |



 

## <a name="remarks"></a>Comentários

Essa interface foi estendida pela interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , herdando todos os métodos e propriedades das interfaces anteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 é definido como 222c4b5d-45D9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

