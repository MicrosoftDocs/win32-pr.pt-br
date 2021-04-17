---
title: Método GetParam IConfigAsfWriter2
description: O método GetParam recupera o valor atual do parâmetro de configuração de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Método GetParam formato de mídia do Windows
- Método GetParam Windows Media Format, interface IConfigAsfWriter2
- IConfigAsfWriter2 interface formato Windows Media, método GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811537"
---
# <a name="iconfigasfwriter2getparam-method"></a>Método IConfigAsfWriter2:: GetParam

O método **GetParam** recupera o valor atual do parâmetro de configuração de filtro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ no\]
</dt> <dd>

Especifica o parâmetro a recuperar. Ele deve ser um valor definido na enumeração do [ \_ \_ \_ parâmetro am ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*pdwParam1* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recupera o valor do parâmetro especificado em *dwParam*.

</dd> <dt>

*pdwParam2* \[ fora\]
</dt> <dd>

Não usado, deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 