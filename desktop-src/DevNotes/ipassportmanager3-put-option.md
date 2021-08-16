---
description: Define uma opção de entrada Microsoft .NET Passport específica.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: 'IPassportManager3: método de ut_Option de:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92a1c432df3f3948a85205e26da64073722ba84dd365ebdcaccf3b80521c517c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827170"
---
# <a name="ipassportmanager3put_option-method"></a>Método de opção IPassportManager3::p UT \_

Define uma opção de entrada Microsoft .NET Passport específica.

> [!Note]  
> O método de **\_ opção Put** pertence à interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) . Este tópico complementa a documentação inicial.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*name* 
</dt> <dd>

A opção de entrada a ser definida. Atualmente, a única opção com suporte é iMode.

</dd> <dt>

*newVal* 
</dt> <dd>

Uma **variante** (VT \_ bool) que especifica o novo valor para a opção. Esse valor pode ser true ou false.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK quando o método for bem sucedido.

## <a name="remarks"></a>Comentários

Esse método é fornecido com versões mais antigas do SDK do Passport.

 

 
