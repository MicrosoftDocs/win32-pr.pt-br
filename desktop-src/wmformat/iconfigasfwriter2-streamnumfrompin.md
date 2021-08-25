---
title: Método IConfigAsfWriter2 StreamNumFromPin
description: O método StreamNumFromPin recupera o número de fluxo associado ao pino de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Formato de mídia do windows do método StreamNumFromPin
- Formato de mídia do windows do método StreamNumFromPin, interface IConfigAsfWriter2
- Formato de mídia da interface IConfigAsfWriter2 , método StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839817"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Método IConfigAsfWriter2::StreamNumFromPin

O **método StreamNumFromPin** recupera o número de fluxo associado ao pino de entrada especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPin* \[ Em\]
</dt> <dd>

Ponteiro para a interface **IPin** no pino de entrada.

</dd> <dt>

*pwStreamNum* \[ out\]
</dt> <dd>

Ponteiro que recebe o número do fluxo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="remarks"></a>Comentários

Às vezes, talvez seja necessário usar as interfaces do SDK Windows Formato de Mídia diretamente para manipular um fluxo antes de executar um grafo de filtro. Como você não pode assumir que um número de fluxo ASF é o mesmo que o número DirectShow de pino, esse método é fornecido.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 