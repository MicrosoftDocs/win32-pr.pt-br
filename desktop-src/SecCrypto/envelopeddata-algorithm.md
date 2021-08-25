---
description: Recupera o algoritmo de criptografia e o comprimento da chave.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: Propriedade EnvelopedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58971f27c271e18cef63f670a74ad0b78bbcb92914d35d9c6ca1f8461dfe15ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874406"
---
# <a name="envelopeddataalgorithm-property"></a>Propriedade EnvelopedData. Algorithm

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade de **algoritmo** recupera o algoritmo de criptografia e o [*comprimento da chave*](../secgloss/k-gly.md).

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**algoritmo**](algorithm.md) que contém o algoritmo de criptografia e o comprimento da chave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
