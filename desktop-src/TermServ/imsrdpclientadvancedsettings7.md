---
title: Interface IMsRdpClientAdvancedSettings7
description: Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings7, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755160"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>Interface IMsRdpClientAdvancedSettings7

Expõe métodos e propriedades que gerenciam as configurações avançadas do controle ActiveX.

Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings7 de IID** para **QueryInterface**.

## <a name="members"></a>Membros

A interface **IMsRdpClientAdvancedSettings7** herda de **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientAdvancedSettings7** tem essas propriedades.



| Propriedade                                                                                                    | Tipo de acesso           | Descrição                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Leitura/gravação<br/> | Especifica ou recupera um valor que indica se o dispositivo de entrada de áudio padrão é redirecionado do cliente para a sessão remota.<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Leitura/gravação<br/> | Especifica ou recupera um valor que indica a configuração do modo de qualidade de áudio para áudio Redirecionado.<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Leitura/gravação<br/> | Especifica ou recupera um valor que indica se SuperPan está habilitado ou desabilitado.<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Leitura/gravação<br/> | Especifica ou recupera um valor que indica o tipo de conexão de rede.<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Leitura/gravação<br/> | Essa propriedade não é usada.<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Leitura/gravação<br/> | Especifica ou recupera um valor que indica o fator de aceleração SuperPan.<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Leitura/gravação<br/> | Especifica ou recupera um valor que indica o modo de reprodução de vídeo.<br/>                                                                    |



 

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

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

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

 

