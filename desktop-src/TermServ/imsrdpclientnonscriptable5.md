---
title: Interface IMsRdpClientNonScriptable5
description: Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota da interface IMsRdpClientNonScriptable5, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec338dbe07c4733bf80207298f23f388bf8f77c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456002"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Interface IMsRdpClientNonScriptable5

Fornece acesso às propriedades não programáveis da sessão remota de um cliente no controle ActiveX Área de Trabalho Remota. Deriva da interface [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) . Os métodos desta interface só podem ser acessados por meio de vtable; Eles não estão disponíveis para uso em clientes programáveis.

Uma instância dessa interface é obtida chamando [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IMsTscAx**](imstscax-interface.md) , passando **\_ IMsRdpClientNonScriptable5 de IID**.

## <a name="members"></a>Membros

A interface **IMsRdpClientNonScriptable5** herda de [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientNonScriptable5** tem essas propriedades.



| Propriedade                                                                                                         | Tipo de acesso           | Descrição                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Leitura/gravação<br/> | Especifica se o controle ActiveX Área de Trabalho Remota pode solicitar credenciais ao usuário.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Somente gravação<br/> | Especifica se o controle ActiveX Área de Trabalho Remota deve desabilitar a barra de conexão.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Leitura/gravação<br/> | Especifica se o controle ActiveX Área de Trabalho Remota não deve verificar os recursos de RemoteApp do servidor.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Somente leitura<br/>  | Especifica o retângulo delimitador do monitor remoto.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Somente leitura<br/>  | Especifica o número de monitores remotos.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Somente leitura<br/>  | Especifica se o layout do monitor remoto é idêntico ao layout do monitor local.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Leitura/gravação<br/> | Especifica se o controle ActiveX Área de Trabalho Remota deve usar vários monitores.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Leitura/gravação<br/> | Essa propriedade não é usada.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

