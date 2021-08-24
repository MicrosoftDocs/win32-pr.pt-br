---
description: Recupera o valor de uma opção Microsoft .NET de login do Passport específica.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: Método IPassportManager3::get_Option
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5d7260e3c13be21f1cc963e1bca15a6126739a0075b94ee11f07d98901efd39b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750036"
---
# <a name="ipassportmanager3get_option-method"></a>Método Option IPassportManager3::get \_

Recupera o valor de uma opção Microsoft .NET de login do Passport específica.

> [!Note]  
> O **método \_ get Option** pertence à interface [**IPassportManager3.**](/previous-versions/ms817681(v=msdn.10)) Este tópico complementa a documentação inicial.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* \[ Em\]
</dt> <dd>

A opção de login a ser recuperada. Atualmente, a única opção com suporte é "iMode".

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Um ponteiro para **uma VARIANT** (VT \_ BOOL) que recebe o valor da opção. Esse valor pode ser True ou False.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK quando o método é bem-sucedido.

## <a name="remarks"></a>Comentários

Esse método é produzido com versões mais antigas do SDK do Passport.

 

 
