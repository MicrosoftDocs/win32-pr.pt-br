---
description: 'Recupera um ponteiro de interface e incrementa a contagem de referência. Esse método implementa o método INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Método CUnknown. NonDelegatingQueryInterface (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e13d9d30c3da208bb702427ee99a9648a7f538ba0d5a6a1b359db41e2cd155
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076006"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>Método CUnknown. NonDelegatingQueryInterface

Recupera um ponteiro de interface e incrementa a contagem de referência. Esse método implementa o método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador da interface.

</dd> <dt>

*ppv* 
</dt> <dd>

Endereço de um ponteiro para receber a interface.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | O objeto não oferece suporte a essa interface.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo** .<br/>              |



 

## <a name="remarks"></a>Comentários

A classe **CUnknown** expõe apenas a interface **IUknown** . Substitua esse método para expor interfaces adicionais. Para obter informações sobre como substituir esse método, consulte [como implementar IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




