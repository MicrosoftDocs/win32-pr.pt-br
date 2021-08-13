---
description: Remove todos os objetos de certificado de uma coleção de destinatários.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Método Recipients. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c956aacd7b61243fbaeb26ed1a29ed0fee4522d83d8b4ef3ac25b3b1921b42a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900803"
---
# <a name="recipientsclear-method"></a>Método Recipients. Clear

\[O método **Clear** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Clear** remove todos os objetos de [**certificado**](certificate.md) de uma coleção de [**destinatários**](recipients.md) .

## <a name="syntax"></a>Sintaxe


```VB
Recipients.Clear()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Um aplicativo que usa esse método deve conter código para manipular uma exceção gerada por esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Destinatários**](recipients.md)
</dt> </dl>

 

 
