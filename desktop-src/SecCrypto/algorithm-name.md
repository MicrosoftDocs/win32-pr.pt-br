---
description: Define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia. Essa é a propriedade padrão.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propriedade Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4d9860e9a3f04f2f17ebcda08a4ec2610c5af3cbb5fbb5e7afa98227264992b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880146"
---
# <a name="algorithmname-property"></a>Propriedade Algorithm.Name

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Name** define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia. Essa é a propriedade padrão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**do \_ \_ algoritmo de criptografia capicor**](capicom-encryption-algorithm.md) que especifica qual algoritmo usar. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                       | Significado                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <dt>**Algoritmo de criptografia CAPICOM \_ \_ \_ RC2**</dt> </dl>    | Use a criptografia RC2.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <dt>**Algoritmo de criptografia capicor \_ \_ \_ RC4**</dt> </dl>    | Use a criptografia RC4.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <dt>**algoritmo de criptografia CAPICOM \_ \_ \_ des**</dt> </dl>    | Use a criptografia DES.<br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <dt>**Algoritmo de criptografia CAPICOM \_ \_ \_ 3DES**</dt> </dl> | Use a criptografia triple DES.<br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <dt>**algoritmo de criptografia capicor \_ \_ \_ AES**</dt> </dl>    | Use o algoritmo AES.<br/>     |



 

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o estado inteiro do objeto é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
