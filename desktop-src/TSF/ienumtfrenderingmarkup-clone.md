---
title: Método Clone IEnumTfRenderingMarkup
description: O método clone IEnumTfRenderingMarkup cria uma cópia do objeto enumerador.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Estrutura de serviços de texto de método de clonagem
- Método clone de serviços de texto text Framework, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, método clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105796339"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>Método IEnumTfRenderingMarkup:: clone

O método **IEnumTfRenderingMarkup:: clone** cria uma cópia do objeto enumerador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ fora\]
</dt> <dd>

\[\]um ponteiro para uma interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>          |
| <dl> <dt>**E \_ falha**</dt> </dl>       | Ocorreu um erro não especificado.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros são inválidos.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Esse método não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

