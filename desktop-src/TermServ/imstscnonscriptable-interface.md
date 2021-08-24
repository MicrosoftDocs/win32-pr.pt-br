---
title: Interface IMsTscNonScriptable
description: Contém propriedades e métodos relacionados à aplicação de uma senha ao Área de Trabalho Remota ActiveX controle.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Interface IMsTscNonScriptable Serviços de Área de Trabalho Remota
- Interface IMsTscNonScriptable Serviços de Área de Trabalho Remota , descrita
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
ms.openlocfilehash: 86ce3b1e921635850e9ffa713c55a812a806ac4e757e772569e7db817410ad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770646"
---
# <a name="imstscnonscriptable-interface"></a>Interface IMsTscNonScriptable

Contém propriedades e métodos relacionados à aplicação de uma senha ao Área de Trabalho Remota ActiveX controle.

O principal uso da interface **IMsTscNonScriptable** é configurar o acesso automático de logon de senha a servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) em cenários em que o controle Área de Trabalho Remota ActiveX está hospedado em um contêiner personalizado escrito. Quando o logon automático é configurado, o usuário não recebe a caixa de Windows logon no momento da conexão.

Em algumas plataformas, os métodos da interface **IMsTscNonScriptable** podem ser usados para especificar senhas em um dos três formatos com suporte:

-   Texto sem formatação
-   Codificado portátil
-   Binário (não acessível) codificado

Observe que uma senha em um formato codificado consiste em duas partes:

-   Parte da senha codificada.
-   Parte do valor de sal.

Ambas as partes são necessárias para definir uma senha codificada. Nem a parte de senha codificada nem a parte do valor de sal devem ser consideradas criptografadas com segurança.

O acesso passível de script para senhas de texto não criptografado está disponível por meio da propriedade [**ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) da interface passível de script [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).

A interface **IMsTscNonScriptable** só pode ser acessada por meio da vtable.

## <a name="members"></a>Membros

A interface **IMsTscNonScriptable** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsTscNonScriptable** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsTscNonScriptable** tem esses métodos.



| Método                                                     | Descrição                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**Resetpassword**](imstscnonscriptable-resetpassword.md) | Redefine todos os estados de senha no controle .<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IMsTscNonScriptable** tem essas propriedades.



| Propriedade                                                                      | Tipo de acesso           | Descrição                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Somente gravação<br/> | O Área de Trabalho Remota ActiveX controle de senha, em formato de texto não criptografado.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Leitura/gravação<br/> | Não há suporte a esta propriedade.<br/>                                   |



 

## <a name="remarks"></a>Comentários

Fornecer uma senha para o controle Área de Trabalho Remota ActiveX é opcional. Se você fornecer uma senha ao controle, deverá aplicar apenas um dos três formatos anteriores ao controle antes de iniciar a conexão com uma chamada ao [**método Conexão.**](imstscax-connect.md)

> [!Note]  
> Você também pode habilitar o logon automático no servidor com a ferramenta de configuração do Serviços de Área de Trabalho Remota (Tscc.msc.) Um administrador pode usar essa ferramenta para atribuir uma senha específica a uma conexão em uma situação em que um logon automatizado é necessário.

 

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

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
| CLSID<br/>                    | CLSID \_ MsRdpClient é definido como 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 é definido como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting é definido como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient2 é definido como 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a é definido como 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting é definido como 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 é definido como 7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a é definido como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting é definido como ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 é definido como 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a é definido como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting é definido como 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 é definido como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting é definido como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 é definido como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting é definido como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 é definido como A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting é definido como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 é definido como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting é definido como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting é definido como 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID MsTscAx é definido como \_ 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting é definido como A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx:: Conexão**](imstscax-connect.md)
</dt> </dl>

 

