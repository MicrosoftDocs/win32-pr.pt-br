---
description: A propriedade timetimestamper recupera a hora Stamper do arquivo executável assinado.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Propriedade SignedCode. timetimestamper
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754589"
---
# <a name="signedcodetimestamper-property"></a>Propriedade SignedCode. timetimestamper

\[A propriedade de **carimbo de data/hora** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A propriedade **Timetimestamper** recupera a hora Stamper do arquivo executável assinado.

## <a name="syntax"></a>Syntax


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**signatário**](signer.md) que fornece acesso ao Stamper de tempo do arquivo executável assinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
