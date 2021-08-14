---
description: A propriedade FileName define ou recupera o caminho para o arquivo executável. Essa é a propriedade padrão.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Propriedade SignedCode. FileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 981ff6e1343f836ef145d1dac8c66b93d7a89c885a04cb2fe024740d7e35a53d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900376"
---
# <a name="signedcodefilename-property"></a>Propriedade SignedCode. FileName

\[A propriedade **filename** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A propriedade **filename** define ou recupera o caminho para o arquivo executável. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Valor da propriedade

O caminho para o arquivo executável.

## <a name="remarks"></a>Comentários

Se o valor da propriedade **filename** for modificado, o estado do objeto [**SignedCode**](signedcode.md) inteiro será redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
