---
description: Define ou recupera a descrição do arquivo executável assinado.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Propriedade SignedCode.Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6046beae61aebaf33ea5eedb6ef2ec643f2edb39dbbedc61372085be2220068b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900346"
---
# <a name="signedcodedescription-property"></a>Propriedade SignedCode.Description

\[A **propriedade Description** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use os Serviços de Invocação de Plataforma (PInvoke) para chamar as funções [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

A **propriedade Description** define ou recupera a descrição do arquivo executável assinado.

## <a name="syntax"></a>Syntax


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Valor da propriedade

A descrição do arquivo executável assinado.

## <a name="remarks"></a>Comentários

A descrição é o texto que aparece na caixa de diálogo Verificação do Authenticode. O texto deve descrever o arquivo executável assinado. Se essa propriedade for **NULL,** a caixa de diálogo exibirá o nome do arquivo executável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
