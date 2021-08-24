---
description: Recupera o número de objetos ExtendedProperty na coleção.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: Propriedade ExtendedProperties.Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c34aa63da5276c573d5c3f260d5d7a5956045813695991756ede6c9f69be29ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007264"
---
# <a name="extendedpropertiescount-property"></a>Propriedade ExtendedProperties.Count

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar a função de API Do Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) e obter as propriedades. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A **propriedade Count** recupera o número de objetos [**ExtendedProperty**](extendedproperty.md) na coleção.

## <a name="syntax"></a>Syntax


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a>Valor da propriedade

O número de [**objetos ExtendedProperty**](extendedproperty.md) na coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
