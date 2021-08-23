---
description: Recupera os dados com hash após chamadas bem-sucedidas para o método de hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Propriedade HashedData. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a6b8b2c8291e793cd88c5d4b0821c036fb6b112beb87e73d4f8ccb8d523deb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006564"
---
# <a name="hasheddatavalue-property"></a>Propriedade HashedData. Value

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **Value** recupera os dados com hash após chamadas bem-sucedidas para o método de [**hash**](hasheddata-hash.md) . O valor de hash é retornado no formato hexadecimal. Essa é a propriedade padrão.

## <a name="syntax"></a>Syntax


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que contém os dados com hash no formato hexadecimal.

## <a name="remarks"></a>Comentários

Para criar o hash de uma grande quantidade de dados, chame o método de [**hash**](hasheddata-hash.md) para cada dado. O hash de cada parte dos dados é concatenado à propriedade **Value** até que a propriedade seja lida. O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
