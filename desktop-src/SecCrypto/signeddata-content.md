---
description: Define ou recupera os dados a serem assinados. Essa é a propriedade padrão.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Propriedade SignedData. Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750742"
---
# <a name="signeddatacontent-property"></a>Propriedade SignedData. Content

\[A propriedade de **conteúdo** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade de **conteúdo** define ou recupera os dados a serem assinados. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Valor da propriedade

Os dados a serem assinados.

## <a name="remarks"></a>Comentários

Essa propriedade deve ser inicializada antes que o método [**Sign**](signeddata-sign.md) seja chamado. Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer assinatura associada ao objeto antes da alteração da propriedade é perdida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
