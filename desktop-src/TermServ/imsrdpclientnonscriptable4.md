---
title: Interface IMsRdpClientNonScriptable4
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable3.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable4, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919207"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>Interface IMsRdpClientNonScriptable4

Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) . Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.

## <a name="members"></a>Membros

A interface **IMsRdpClientNonScriptable4** herda de [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientNonScriptable4** tem essas propriedades.



| Propriedade                                                                                                         | Tipo de acesso           | Descrição                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowCredentialSaving**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Leitura/gravação<br/> | Especifica se a caixa de diálogo credenciais exibe uma caixa de seleção para habilitar o salvamento de credenciais.<br/>                                                                                        |
| [**LaunchedViaClientShellInterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Leitura/gravação<br/> | Especifica se o usuário iniciou o controle de cliente usando a interface de Acesso via Web de trabalho remota.<br/>                                                                                                  |
| [**MarkRdpSettingsSecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Leitura/gravação<br/> | Especifica se as configurações de RDP são marcadas como seguras.<br/>                                                                                                                                          |
| [**PromptForCredsOnClient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Leitura/gravação<br/> | Especifica se o controle de cliente exibe uma caixa de diálogo solicitando as credenciais.<br/>                                                                                                      |
| [**PublisherCertificateChain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Leitura/gravação<br/> | Especifica a cadeia de certificados do Publicador. A cadeia é armazenada em uma variante do tipo VT \_ ByRef que contém um ponteiro para uma estrutura de [**contexto de \_ cadeia \_ de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .<br/> |
| [**RedirectionWarningType**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Leitura/gravação<br/> | Controla a presença e a aparência da caixa de diálogo de redirecionamento.<br/>                                                                                                                           |
| [**TrustedZoneSite**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Leitura/gravação<br/> | Especifica se o site do qual o usuário iniciou a conexão está na lista de sites confiáveis do computador cliente.<br/>                                                                |
| [**WarnAboutPrinterRedirection**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Leitura/gravação<br/> | Especifica se a caixa de diálogo redirecionamento exibe uma mensagem sobre o redirecionamento de impressora antes de iniciar uma sessão.<br/>                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient6 é definido como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting é definido como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 é definido como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

