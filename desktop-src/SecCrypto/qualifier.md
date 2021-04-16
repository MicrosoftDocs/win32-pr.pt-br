---
description: Representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Objeto de qualificador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752531"
---
# <a name="qualifier-object"></a>Objeto de qualificador

\[O objeto de **qualificador** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

O objeto de **qualificador** representa um ponteiro de declaração de prática de certificação (CPS) ou um qualificador de aviso do usuário.

## <a name="when-to-use"></a>Quando usar

O objeto de **qualificador** é usado para executar as seguintes tarefas:

-   Recupere o identificador de objeto do qualificador.
-   Recupere o Uniform Resource Identifier (URI) que aponta para um CPS publicado pela [*autoridade de certificação*](../secgloss/c-gly.md) (CA).
-   Recupere o nome da organização associada ao qualificador.
-   Recupere o nome e o conteúdo de um aviso do usuário.

## <a name="members"></a>Membros

O objeto de **qualificador** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **qualificador** tem essas propriedades.



| Propriedade                                                          | Tipo de acesso          | Descrição                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o URI que aponta para um CPS publicado pela autoridade de certificação.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o conteúdo do aviso do usuário. Esta propriedade pode estar vazia.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Somente leitura<br/> | Recupera um objeto **NoticeNumbers** que contém a coleção de números de aviso do usuário. Esta propriedade pode estar vazia.<br/>    |
| [**OIDs**](qualifier-oid.md)<br/>                           | Somente leitura<br/> | Recupera um objeto [**OID**](oid.md) que identifica o qualificador. Essa é a propriedade padrão.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Somente leitura<br/> | Recupera uma cadeia de caracteres que contém o nome da organização associada ao qualificador. Esta propriedade pode estar vazia.<br/> |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **qualificador** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
