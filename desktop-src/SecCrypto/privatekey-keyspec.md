---
description: Recupera a especificação da chave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: Propriedade PrivateKey.KeySpec
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b28694c639260fccfce5d703e43aea4040fe0966cb9f330c2dc625892bd6907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978010"
---
# <a name="privatekeykeyspec-property"></a>Propriedade PrivateKey.KeySpec

\[A **propriedade KeySpec** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a propriedade X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade KeySpec** recupera a especificação da chave.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a>Valor da propriedade

Um valor da [**enumeração CAPICOM \_ KEY \_ SPEC**](capicom-key-spec.md) que indica a especificação da chave. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                        | Significado                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM \_ KEY \_ SPEC \_ KEYEXCHANGE**</dt> </dl> | A chave pode ser usada para criptografia e assinatura.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**ASSINATURA DE ESPECIFICAÇÃO \_ \_ DE CHAVE CAPICOM \_**</dt> </dl>       | A chave só pode ser usada para assinatura.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Privatekey**](privatekey.md)
</dt> </dl>

 

 
