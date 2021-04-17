---
description: Define ou recupera o conteúdo de texto não criptografado de uma mensagem a ser envelopada. Essa é a propriedade padrão.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Propriedade EnvelopedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751318"
---
# <a name="envelopeddatacontent-property"></a>Propriedade EnvelopedData. Content

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade de **conteúdo** define ou recupera o conteúdo de texto não criptografado de uma mensagem a ser envelopada. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valor da propriedade

O conteúdo de texto não criptografado de uma mensagem a ser envelopada.

## <a name="remarks"></a>Comentários

A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](envelopeddata-encrypt.md) seja chamado. Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
