---
description: Define ou recupera um valor booliano que indica se o certificado está arquivado.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propriedade Certificate. Arquived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771945"
---
# <a name="certificatearchived-property"></a>Propriedade Certificate. Arquived

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **arquivada** define ou recupera um valor booliano que indica se o certificado está arquivado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliano que indica se o certificado é arquivado. Se for **true**, o certificado será arquivado. Observe que a alteração do valor de **false** para **true** arquiva o certificado.

## <a name="remarks"></a>Comentários

Essa propriedade gera CAPICOM \_ E \_ não \_ são permitidos quando são inseridos em script de um aplicativo baseado na Web.

> [!Note]  
> Um certificado arquivado não é visível na interface do usuário do gerenciamento de certificados. Além disso, os certificados arquivados não serão incluídos no método [**Store. Open**](store-open.md) , a menos que o capicote \_ Store \_ Open \_ include \_ arquivo morto seja especificado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
