---
description: A propriedade Result recupera um valor que indica se o certificado é válido. Essa é a propriedade padrão.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Propriedade CertificateStatus. Result
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755313"
---
# <a name="certificatestatusresult-property"></a>Propriedade CertificateStatus. Result

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **Result** recupera um valor que indica se o certificado é válido. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se **for true**, o certificado será válido. A validade do certificado é verificada usando a configuração atual da propriedade [**CheckFlag**](certificatestatus-checkflag.md) e as várias configurações de política.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
