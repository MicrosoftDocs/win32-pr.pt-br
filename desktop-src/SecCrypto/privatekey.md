---
description: Representa a chave privada associada a um certificado.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: Objeto PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764615"
---
# <a name="privatekey-object"></a>Objeto PrivateKey

\[O objeto **PrivateKey** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **PrivateKey** representa a [*chave privada*](../secgloss/p-gly.md) associada a um certificado.

## <a name="when-to-use"></a>Quando usar

O objeto **PrivateKey** é usado para executar as seguintes tarefas:

-   Recupere informações sobre a chave privada.
-   Abra o contêiner de chave privada.
-   Exclua a chave privada.

## <a name="members"></a>Membros

O objeto **PrivateKey** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **PrivateKey** tem esses métodos.



| Método                                                  | Descrição                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Apagar**](privatekey-delete.md)                     | Exclui o contêiner de chave privada referenciado pelo objeto **PrivateKey** .<br/>                                                                                |
| [**Isacessível**](privatekey-isaccessible.md)         | Recupera um valor booliano que indica se a chave privada pode ser acessada pelo usuário. Se for true, o usuário poderá acessar a chave privada.<br/>                 |
| [**IsExportable**](privatekey-isexportable.md)         | Recupera um valor booliano que indica se a chave privada pode ser exportada. Se for true, a chave privada poderá ser exportada.<br/>                               |
| [**IsHardwareDevice**](privatekey-ishardwaredevice.md) | Recupera um valor booliano que indica se a chave privada está armazenada em um dispositivo de hardware. Se for true, a chave privada será armazenada em um dispositivo de hardware.<br/> |
| [**Ismachinekeyset**](privatekey-ismachinekeyset.md)   | Recupera um valor booliano que indica se a chave privada é uma chave de computador. Se for true, a chave privada será uma chave de computador.<br/>                             |
| [**Isprotegeu**](privatekey-isprotected.md)           | Recupera um valor booliano que indica se a chave privada está protegida. Se for true, a chave privada será protegida.<br/>                                     |
| [**IsRemovable**](privatekey-isremovable.md)           | Recupera um valor booliano que indica se a chave privada está em um dispositivo removível. Se for true, a chave privada estará em um dispositivo removível.<br/>             |
| [**Aberto**](privatekey-open.md)                         | Acessa um contêiner de chave existente.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriedades

O objeto **PrivateKey** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [**ContainerName**](privatekey-containername.md)<br/>             | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome do contêiner da chave privada. Essa é a propriedade padrão.<br/> |
| [**KeySpec**](privatekey-keyspec.md)<br/>                         | Somente leitura<br/> | Recupera a especificação de chave.<br/>                                                               |
| [**ProviderName**](privatekey-providername.md)<br/>               | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome do CSP.<br/>                                          |
| [**ProviderType**](privatekey-providertype.md)<br/>               | Somente leitura<br/> | Recupera um valor de enumeração que especifica o tipo de provedor.<br/>                            |
| [**UniqueContainerName**](privatekey-uniquecontainername.md)<br/> | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome exclusivo do contêiner de chave privada.<br/>                        |



 

## <a name="remarks"></a>Comentários

O objeto **PrivateKey** pode ser criado e é seguro para scripts. O ProgID do objeto **PrivateKey** é CAPICOM. PrivateKey. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
