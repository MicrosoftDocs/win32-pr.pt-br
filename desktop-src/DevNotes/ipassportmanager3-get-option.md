---
description: Recupera o valor de uma opção de entrada específica do Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Método IPassportManager3:: get_Option'
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
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370356"
---
# <a name="ipassportmanager3get_option-method"></a>Método de opção IPassportManager3:: get \_

Recupera o valor de uma opção de entrada específica do Microsoft .NET Passport.

> [!Note]  
> O método **Get \_ Option** pertence à interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Este tópico complementa a documentação inicial.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

A opção de entrada a ser recuperada. Atualmente, a única opção com suporte é "iMode".

</dd> <dt>

*PVal* \[ fora\]
</dt> <dd>

Um ponteiro para uma **variante** (VT \_ bool) que recebe o valor da opção. Esse valor pode ser true ou false.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK quando o método for bem sucedido.

## <a name="remarks"></a>Comentários

Esse método é fornecido com versões mais antigas do SDK do Passport.

 

 
