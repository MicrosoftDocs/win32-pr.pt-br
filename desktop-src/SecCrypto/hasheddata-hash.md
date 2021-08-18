---
description: Cria um hash da cadeia de caracteres especificada.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Método HashedData. hash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2828f54f754591d1b0027a6c892dc57e8b5cdfecc5e9759985b74b1dffef9fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006574"
---
# <a name="hasheddatahash-method"></a>Método HashedData. hash

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método de **hash** cria um hash da cadeia de caracteres especificada.

## <a name="syntax"></a>Sintaxe


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* 
</dt> <dd>

Cadeia de caracteres que contém o valor para hash.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para criar o hash de uma grande quantidade de dados, chame o método de **hash** para cada dado. O hash de cada parte dos dados é concatenado à propriedade [**Value**](hasheddata-value.md) até que a propriedade seja lida. O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
