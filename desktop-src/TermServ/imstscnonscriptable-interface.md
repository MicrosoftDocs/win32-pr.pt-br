---
title: Interface IMsTscNonScriptable
description: Contém propriedades e métodos relacionados ao aplicativo de uma senha para o controle ActiveX Área de Trabalho Remota.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota da interface IMsTscNonScriptable, descrita
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92372f7ea9479f7fcdd632546a0bd7dd2f0b465e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811910"
---
# <a name="imstscnonscriptable-interface"></a>Interface IMsTscNonScriptable

Contém propriedades e métodos relacionados ao aplicativo de uma senha para o controle ActiveX Área de Trabalho Remota.

O principal uso da interface **IMsTscNonScriptable** é configurar o acesso de logon automático de senha para servidores Host da Sessão da Área de Trabalho Remota (host da Sessão RD) em cenários nos quais o controle ActiveX área de trabalho remota está hospedado em um contêiner de escrita personalizada. Quando o logon automático é configurado, o usuário não recebe a caixa de diálogo de logon do Windows no momento da conexão.

Em algumas plataformas, os métodos da interface **IMsTscNonScriptable** podem ser usados para especificar senhas em um dos três formatos com suporte:

-   Texto sem formatação
-   Codificado em portátil
-   Binário (não Portable) codificado

Observe que uma senha em um formato codificado consiste em duas partes:

-   Parte da senha codificada.
-   Parte do valor de Salt.

Ambas as partes são necessárias para definir uma senha codificada. Nem a parte da senha codificada nem a parte do valor de Salt deve ser considerada criptografada com segurança.

O acesso programável a senhas de texto não criptografado está disponível por meio da propriedade [**clearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) da interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)programável.

A interface **IMsTscNonScriptable** pode ser acessada somente por meio de vtable.

## <a name="members"></a>Membros

A interface **IMsTscNonScriptable** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsTscNonScriptable** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsTscNonScriptable** tem esses métodos.



| Método                                                     | Descrição                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | Redefine todos os Estados de senha no controle.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IMsTscNonScriptable** tem essas propriedades.



| Propriedade                                                                      | Tipo de acesso           | Descrição                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Somente gravação<br/> | A senha do controle ActiveX Área de Trabalho Remota, em formato de texto sem formatação.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |



 

## <a name="remarks"></a>Comentários

Fornecer uma senha para o controle ActiveX Área de Trabalho Remota é opcional. Se você fornecer uma senha para o controle, deverá aplicar apenas um dos três formatos anteriores ao controle antes de iniciar a conexão com uma chamada para o método [**Connect**](imstscax-connect.md) .

> [!Note]  
> Você também pode habilitar o logon automático no servidor com a ferramenta de configuração de Serviços de Área de Trabalho Remota (TSCC. msc). um administrador pode usar essa ferramenta para atribuir uma senha específica a uma conexão em uma situação em que um logon automatizado é necessário.

 

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

A interface **IMsTscNonScriptable** foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient é definido como 791fa017-2de3-492E-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient2 é definido como 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a é definido como 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting é definido como 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 é definido como 7584C670-2274-4efb-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a é definido como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting é definido como ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 é definido como 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a é definido como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting é definido como 6AE29350-321B-42BE-bbe5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 é definido como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting é definido como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 é definido como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting é definido como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472e-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting é definido como 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx é definido como 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting é definido como A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx:: conectar**](imstscax-connect.md)
</dt> </dl>

 

