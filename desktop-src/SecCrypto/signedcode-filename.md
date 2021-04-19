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
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756854"
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
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
