---
description: Representa uma coleção de qualificadores.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Objeto Qualifiers (IADs. h)
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
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784143"
---
# <a name="qualifiers-object"></a>Objeto Qualifiers

\[O objeto **Qualifiers** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]

O objeto **Qualifiers** representa uma coleção de qualificadores.

## <a name="when-to-use"></a>Quando usar

O objeto **Qualifiers** é usado para executar as seguintes tarefas:

-   Recupere uma propriedade estendida específica da coleção.
-   Recupere o número de propriedades estendidas na coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **Qualifiers** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Qualifiers** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](qualifiers-count.md)<br/>       | Somente leitura<br/> | Recupera o número de qualificadores na coleção.<br/>                                                                                                                                                                |
| [**Item**](qualifiers-item.md)<br/>         | Somente leitura<br/> | Recupera um objeto de [**qualificador**](qualifier.md) que representa o qualificador indexado da coleção. Essa é a propriedade padrão.<br/>                                                                             |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto **Qualifiers** .

A propriedade de objeto [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) capicor retorna um objeto **Qualifiers** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| parâmetro<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
