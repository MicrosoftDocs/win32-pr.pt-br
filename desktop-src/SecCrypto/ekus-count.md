---
description: Recupera o número de objetos EKU na coleção.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Propriedade EKUs. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4ef512c62058d2f4726c21aa8631fef5230ec35ecfe39a3b8dc5470fc93b74e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767160"
---
# <a name="ekuscount-property"></a>Propriedade EKUs. Count

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Count** recupera o número de objetos [**EKU**](eku.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de objetos [**EKU**](eku.md) na coleção. Cada objeto **EKU** representa uma única propriedade EKU (uso estendido de chave) de um certificado.

## <a name="remarks"></a>Comentários

A propriedade **Count** pode ser usada para especificar o último objeto [**EKU**](eku.md) em uma coleção ao recuperar um objeto **EKU** específico usando a propriedade [**EKUs. Item**](ekus-item.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
