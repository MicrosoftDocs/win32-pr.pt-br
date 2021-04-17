---
description: Representa uma cadeia de certificados confiáveis.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Objeto chain
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780169"
---
# <a name="chain-object"></a>Objeto chain

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto **Chain** representa uma cadeia de certificados confiáveis.

Esse objeto fornece propriedades e métodos para criar uma cadeia de certificados confiáveis para verificar a validade dos certificados. A cadeia é criada usando o valor da propriedade [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) e as configurações de política de um objeto [**CertificateStatus**](certificatestatus.md) .

O objeto **Chain** expõe as seguintes interfaces:

-   **IChain2**: introduzido no capicom 2,0.
-   **IChain**: introduzido no capicom 1,0.

## <a name="when-to-use"></a>Quando usar

O objeto **Chain** é usado para executar as seguintes tarefas:

-   Crie uma cadeia de certificados confiáveis.
-   Obtenha os OIDs de todas as políticas de certificado e de aplicativo válidas para a cadeia.
-   Verifique o status dos certificados na cadeia.
-   Obter informações de erro estendidas.
-   Recupere a coleção de certificados na cadeia.

## <a name="members"></a>Membros

O objeto **Chain** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Chain** tem esses métodos.



| Método                                                   | Descrição                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de aplicativo válidos para a cadeia.<br/> (Herdado de **ChainIChain2**)                                                                                                                                                          |
| [**Integrado**](chain-build.md)                             | Cria uma cadeia de verificação de certificado de um certificado final para o [*certificado raiz*](../secgloss/r-gly.md)confiável, retornando um valor booliano que indica a validade geral da cadeia.<br/> (Herdado de **ChainIChain2IChain**) |
| [**CertificatePolicies**](chain-certificatepolicies.md) | Retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de certificado válidos para a cadeia.<br/> (Herdado de **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Retorna uma cadeia de caracteres que contém informações de erro adicionais sobre a entrada indexada.<br/> (Herdado de **ChainIChain2**)                                                                                                                                                                                 |



 

### <a name="properties"></a>Propriedades

O objeto **Chain** tem essas propriedades.



| Propriedade                                              | Tipo de acesso          | Descrição                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](chain-certificates.md)<br/> | Somente leitura<br/> | Recupera uma coleção de [**certificados**](certificates.md) que representa os certificados na cadeia. Essa é a propriedade padrão.<br/> (Herdado de **ChainIChain2IChain**) |
| [**Status**](chain-status.md)<br/>             | Somente leitura<br/> | Recupera o status de validade da cadeia ou um certificado específico na cadeia.<br/> (Herdado de **ChainIChain2IChain**)                                                       |



 

## <a name="remarks"></a>Comentários

O objeto **Chain** pode ser criado e é seguro para scripts. O ProgID do objeto de **cadeia** é "CAPICOM. Chain. 2 ".

**CAPICOM 1. *x*:** a ProgID do objeto de **cadeia** é CAPICOM. Cadeia. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
