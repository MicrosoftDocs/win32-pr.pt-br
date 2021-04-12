---
title: Método IConfigAsfWriter2 StreamNumFromPin
description: O método StreamNumFromPin recupera o número de fluxo associado ao PIN de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Formato de mídia do Windows do método StreamNumFromPin
- Método StreamNumFromPin Windows Media Format, interface IConfigAsfWriter2
- Formato de mídia do Windows de interface IConfigAsfWriter2, método StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366150"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Método IConfigAsfWriter2:: StreamNumFromPin

O método **StreamNumFromPin** recupera o número de fluxo associado ao PIN de entrada especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* \[ no\]
</dt> <dd>

Ponteiro para a interface **IPin** no pino de entrada.

</dd> <dt>

*pwStreamNum* \[ fora\]
</dt> <dd>

Ponteiro que recebe o número do fluxo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Às vezes, talvez seja necessário usar as interfaces do Windows Media Format SDK diretamente para manipular um fluxo antes de executar um gráfico de filtro. Como você não pode pressupor que um número de fluxo de ASF seja o mesmo que o número de PIN do DirectShow, esse método é fornecido.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 