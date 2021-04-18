---
description: Cria uma assinatura de carimbo de data/hora Authenticode no arquivo executável assinado especificado na propriedade SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Método SignedCode. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760380"
---
# <a name="signedcodetimestamp-method"></a>Método SignedCode. Timestamp

\[O método **timestamp** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método timestamp cria uma assinatura de carimbo de data **/** hora Authenticode no arquivo executável assinado especificado na propriedade **SignedCode. FileName** . Esse carimbo de data/hora é uma assinatura de contador no arquivo executável assinado que é executado por uma autoridade de carimbo de data/hora.

## <a name="syntax"></a>Sintaxe


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*URL* \[ do no\]
</dt> <dd>

Uma cadeia de caracteres que contém a URL do servidor de carimbo de data/hora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um carimbo de data/hora estende a validade de um certificado verificando se o arquivo executável foi assinado no momento em que estava carimbado.

Antes que esse método possa ser chamado, o arquivo executável assinado deve ser marcado com carimbo de data/hora devem ser especificados na propriedade **SignedCode. FileName** e o método [**SignedCode. Sign**](signedcode-sign.md) deve ser chamado para assinar o arquivo executável.

Se o arquivo executável assinado já estiver com carimbo de data/hora, esse método substituirá o carimbo de data/hora existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
