---
description: Cria uma cadeia de verificação de certificado de um certificado final para o certificado raiz confiável e retorna um valor booliano que indica a validade geral da cadeia.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Método IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754502"
---
# <a name="ichain2build-method"></a>Método IChain2:: Build

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Build** cria uma cadeia de verificação de certificado de um certificado final para o [*certificado raiz*](../secgloss/r-gly.md) confiável e retorna um valor booliano que indica a validade geral da cadeia.

## <a name="syntax"></a>Sintaxe


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Certificado* \[ do no\]
</dt> <dd>

Um objeto de [**certificado**](certificate.md) que representa o certificado final no qual a cadeia de verificação deve ser criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um valor booliano que indica a validade geral da cadeia. A validade geral se baseia na política de verificação de validade em vigor.

## <a name="remarks"></a>Comentários

A cadeia é criada usando a propriedade [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , bem como as políticas de aplicativo e certificado especificadas por um objeto [**CertificateStatus**](certificatestatus.md) . A coleção retornada é ordenada; o primeiro certificado na coleção, **Certificates. Item**(1), é o certificado final da cadeia. O último certificado na coleção, **Certificates. Item**(**Certificates. Count**), é o [*certificado raiz*](../secgloss/r-gly.md) da cadeia. **Certificates. Item**(0) representa a cadeia inteira.

Cada vez que o método **Chain. Build** é chamado, o [*estado*](../secgloss/s-gly.md) do objeto de [**cadeia**](chain.md) é redefinido.

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
</dt> <dt>

[**Cadeia**](chain.md)
</dt> </dl>

 

 
