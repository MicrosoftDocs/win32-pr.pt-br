---
description: A propriedade TimeStamper recupera o carimbo de data/hora do arquivo executável assinado.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Propriedade SignedCode.TimeStamper
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
ms.openlocfilehash: b5bd6f9376f74d46373f6731c66b2452503c6105fff31ce28b4fc76ac126c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899345"
---
# <a name="signedcodetimestamper-property"></a>Propriedade SignedCode.TimeStamper

\[A **propriedade TimeStamper** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use os Serviços de Invocação de Plataforma (PInvoke) para chamar as funções [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A **propriedade TimeStamper** recupera o carimbo de data/hora do arquivo executável assinado.

## <a name="syntax"></a>Syntax


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto Signer**](signer.md) que fornece acesso ao carimbo de data/hora do arquivo executável assinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
