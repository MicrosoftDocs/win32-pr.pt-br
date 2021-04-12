---
title: Método IDCompositionMatrixTransform setmatrixelement (int, int, IDCompositionAnimation)
description: Anima o valor de um elemento da matriz dessa transformação 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Método setmatrixelement DirectComposition
- Método setmatrixelement DirectComposition, interface IDCompositionMatrixTransform
- IDCompositionMatrixTransform interface DirectComposition, método setmatrixelement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366447"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Método IDCompositionMatrixTransform:: setmatrixelement (int, int, IDCompositionAnimation \* )

Anima o valor de um elemento da matriz dessa transformação 2D.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*linha* \[ de no\]
</dt> <dd>

O índice de linha do elemento a ser alterado. Esse valor deve estar entre 0 e 2, inclusive.

</dd> <dt>

*coluna* \[ no\]
</dt> <dd>

O índice de coluna do elemento a ser alterado. Esse valor deve estar entre 0 e 1, inclusive.

</dd> <dt>

*animação* \[ no\]
</dt> <dd>

Uma animação que representa como o valor do elemento especificado muda ao longo do tempo. Esse parâmetro não deve ser nulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, ela retornará S \_ OK. Caso contrário, ele retorna um código de erro **HRESULT** . Consulte [códigos de erro DirectComposition](directcomposition-error-codes.md) para obter uma lista de códigos de erro.

## <a name="remarks"></a>Comentários

Esse método faz uma cópia da animação especificada. Se o objeto referenciado pelo parâmetro de *animação* for alterado depois de chamar esse método, a alteração não afetará o elemento, a menos que esse método seja chamado novamente. Se o elemento foi animado anteriormente, chamar esse método substituirá a animação anterior pela nova animação.

Esse método falhará se a *animação* for um ponteiro inválido ou se não tiver sido criada pela mesma interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que a transformação afetada. A interface não pode ser uma implementação personalizada; somente interfaces criadas pelo Microsoft DirectComposition podem ser usadas com esse método.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 