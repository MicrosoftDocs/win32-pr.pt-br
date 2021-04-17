---
description: Define ou recupera a URL de uma descrição do arquivo executável assinado.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Propriedade SignedCode. DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779943"
---
# <a name="signedcodedescriptionurl-property"></a>Propriedade SignedCode. DescriptionURL

\[A propriedade **DescriptionURL** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A propriedade **DescriptionURL** define ou recupera a URL de uma descrição do arquivo executável assinado.

## <a name="syntax"></a>Sintaxe


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Valor da propriedade

A URL de uma descrição do arquivo executável assinado.

## <a name="remarks"></a>Comentários

O **DescriptionURL** é a URL para a qual a [**Descrição**](signedcode-description.md) aparece nos links da caixa de diálogo verificação de Authenticode. Se essa propriedade for **nula**, a **Descrição** não funcionará como um link.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
