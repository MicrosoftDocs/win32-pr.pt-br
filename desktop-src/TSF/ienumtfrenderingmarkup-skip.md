---
title: Método IEnumTfRenderingMarkup Skip
description: O método IEnumTfRenderingMarkup Skip Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignorar a estrutura de serviços de texto de método
- Ignorar método texto estrutura de serviços, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, método Skip
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638459"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>Método IEnumTfRenderingMarkup:: Skip

O método **IEnumTfRenderingMarkup:: Skip** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulCount* \[ no\]
</dt> <dd>

\[in \] especifica o número de elementos a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                   | Descrição                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O método foi bem-sucedido.<br/>                                                                              |
| <dl> <dt>**\_falso**</dt> </dl> | O método atingiu o final da enumeração antes que o número especificado de elementos pudesse ser ignorado.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Esse método não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

 





