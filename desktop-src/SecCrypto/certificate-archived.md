---
description: Define ou recupera um valor booliana que indica se o certificado está arquivado.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propriedade Certificate.Archived
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
# <a name="certificatearchived-property"></a>Propriedade Certificate.Archived

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade Archived** define ou recupera um valor booliana que indica se o certificado está arquivado.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Um valor booliana que indica se o certificado está arquivado. Se **true**, o certificado será arquivado. Observe que alterar o valor de **false para** **verdadeiro arquiva** o certificado.

## <a name="remarks"></a>Comentários

Essa propriedade gera CAPICOM \_ E NOT ALLOWED quando é roteado por script de um aplicativo baseado na \_ \_ Web.

> [!Note]  
> Um certificado arquivado não está visível na interface do usuário de gerenciamento de certificados. Além disso, os certificados arquivados não serão incluídos no [**método Store.Open,**](store-open.md) a menos que CAPICOM \_ STORE OPEN INCLUDE \_ \_ \_ ARCHIVED seja especificado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
