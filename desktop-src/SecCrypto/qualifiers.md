---
description: Representa uma coleção de qualificadores.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Objeto Qualifiers (Iads.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f68dbeefefbe675199522dfbc5b1dab81b8a2840fa8b7d5189c72b811fcba7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900952"
---
# <a name="qualifiers-object"></a>Objeto Qualifiers

\[O **objeto Qualificadores** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use a Classe [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para Políticas de Certificado para processar qualificadores que fazem parte das informações de política na extensão políticas de certificado.\]

O **objeto Qualificadores** representa uma coleção de qualificadores.

## <a name="when-to-use"></a>Quando usar

O **objeto Qualificadores** é usado para executar as seguintes tarefas:

-   Recupere uma propriedade estendida específica da coleção.
-   Recupere o número de propriedades estendidas na coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O **objeto Qualificadores** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Qualificadores** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contagem**](qualifiers-count.md)<br/>       | Somente leitura<br/> | Recupera o número de qualificadores na coleção.<br/>                                                                                                                                                                |
| [**Item**](qualifiers-item.md)<br/>         | Somente leitura<br/> | Recupera um [**objeto Qualificador**](qualifier.md) que representa o qualificador indexado da coleção. Essa é a propriedade padrão.<br/>                                                                             |



 

## <a name="remarks"></a>Comentários

O **objeto Qualificadores** não pode ser criado.

A [**propriedade de objeto CAPICOM PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) retorna um objeto **Qualifiers.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| parâmetro<br/>          | <dl> <dt>Iads.h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
