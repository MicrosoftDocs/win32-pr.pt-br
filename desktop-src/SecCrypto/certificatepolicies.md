---
description: Uma coleção de objetos PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objeto CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784154"
---
# <a name="certificatepolicies-object"></a>Objeto CertificatePolicies

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para as políticas de certificado para recuperar as políticas de certificado.\]

O objeto **CertificatePolicies** representa uma coleção de objetos [**PolicyInformation**](policyinformation.md) . Cada objeto [**PolicyInformation**](policyinformation.md) representa uma única política de certificado.

## <a name="when-to-use"></a>Quando usar

O objeto **CertificatePolicies** é usado para executar as seguintes tarefas:

-   Recupere o número de políticas de certificado na coleção.
-   Recupere um objeto [**PolicyInformation**](policyinformation.md) específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto **CertificatePolicies** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **CertificatePolicies** tem essas propriedades.



| Propriedade                                                    | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](certificatepolicies-count.md)<br/>       | Somente leitura<br/> | Recupera o número de objetos [**PolicyInformation**](policyinformation.md) na coleção.<br/>                                                                                                                    |
| [**Item**](certificatepolicies-item.md)<br/>         | Somente leitura<br/> | Recupera um objeto [**PolicyInformation**](policyinformation.md) que representa a política de certificado indexado da coleção. Essa é a propriedade padrão.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

O objeto **CertificatePolicies** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
