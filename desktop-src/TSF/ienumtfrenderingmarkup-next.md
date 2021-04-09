---
title: Método Next IEnumTfRenderingMarkup
description: O método Next IEnumTfRenderingMarkup Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Próxima método de estrutura de serviços de texto
- Próxima método de estrutura de serviços de texto, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, próximo método
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007797"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>Método IEnumTfRenderingMarkup:: Next

O método **IEnumTfRenderingMarkup:: Next** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulCount* \[ fora\]
</dt> <dd>

\[out \] especifica o número de elementos a serem obtidos.

</dd> <dt>

*ppElement* \[ fora\]
</dt> <dd>

\[ponteiro de saída \] para uma matriz de estruturas de [ \_ RENDERINGMARKUP de TF](/windows/desktop/TSF/tf-renderingmarkup) . Essa matriz deve ter pelo menos elementos *ulCount* de tamanho.

</dd> <dt>

*pcFetched* \[ fora\]
</dt> <dd>

\[\]ponteiro de saída para um valor ULONG que recebe o número de elementos realmente obtidos. Esse valor pode ser menor que o número de itens solicitados. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                                                                               |
| <dl> <dt>**\_falso**</dt> </dl>      | O método atingiu o final da enumeração antes que o número especificado de elementos pudesse ser obtido.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros são inválidos.<br/>                                                                      |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Esse método não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

