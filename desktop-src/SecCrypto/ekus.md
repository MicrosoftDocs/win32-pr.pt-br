---
description: Representa uma coleção de objetos EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Objeto EKUs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5258a37ac32e663b45bb2a82f8b0691cca3e1e76c303e8d4f9b7156e4f5a423e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767079"
---
# <a name="ekus-object"></a>Objeto EKUs

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **objeto EKUs** representa uma coleção de [**objetos EKU.**](eku.md) Cada [**objeto EKU**](eku.md) representa uma única propriedade de EKU (uso estendido de chave) de um certificado.

## <a name="when-to-use"></a>Quando usar

A **coleção EKUs** é usada para executar as seguintes tarefas:

-   Recupere o número de propriedades de EKU na coleção.
-   Recupere um objeto [**EKU**](eku.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O **objeto EKUs** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto EKUs** tem essas propriedades.



| Propriedade                                     | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade está oculta no Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contagem**](ekus-count.md)<br/>       | Somente leitura<br/> | Recupera o número de [**objetos EKU**](eku.md) na coleção.<br/>                                                                                                                                                |
| [**Item**](ekus-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto [**EKU**](eku.md) que representa a propriedade de EKU indexada. Essa é a propriedade padrão.<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentários

Essa coleção é recuperada pela [**propriedade ExtendedKeyUsage.EKUs.**](extendedkeyusage-ekus.md)

O **objeto EKUs** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
