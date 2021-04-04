---
title: Interface IMsRdpClient5
description: Fornece os métodos e as propriedades necessários para configurar e usar o controle de cliente. Deriva da interface IMsRdpClient4.
ms.assetid: d3fc5e67-f4d9-4d80-b572-8fc3e660571e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5
- Serviços de Área de Trabalho Remota da interface IMsRdpClient5, descrita
topic_type:
- apiref
api_name:
- IMsRdpClient5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1005fba795c8926052dd8a42e13533e6b3319e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085304"
---
# <a name="imsrdpclient5-interface"></a>Interface IMsRdpClient5

Fornece os métodos e as propriedades necessários para configurar e usar o controle de cliente. Deriva da interface [**IMsRdpClient4**](imsrdpclient4.md) .

## <a name="members"></a>Membros

A interface **IMsRdpClient5** herda de [**IMsRdpClient4**](imsrdpclient4.md). **IMsRdpClient5** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpClient5** tem esses métodos.



| Método                                                           | Descrição                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------|
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) | Recupera os códigos de erro e as mensagens de erro.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpClient5** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso          | Descrição                                                                                         |
|:------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------|
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/> | Somente leitura<br/> | A interface para [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).<br/> |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>   | Somente leitura<br/> | As configurações do cliente para o iniciador do portal da Web.<br/>                                         |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>         | Somente leitura<br/> | A configuração do RemoteApp do cliente.<br/>                                                            |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/> | Somente leitura<br/> | A configuração do gateway RD do cliente.<br/>                                                           |



 

## <a name="remarks"></a>Comentários

A interface **IMsRdpClient5** foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient5 é definido como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting é definido como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 é definido como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting é definido como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





