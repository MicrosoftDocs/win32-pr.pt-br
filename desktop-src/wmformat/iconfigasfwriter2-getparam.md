---
title: Método GetParam IConfigAsfWriter2
description: O método GetParam recupera o valor atual do parâmetro de configuração de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Formato de mídia do windows do método GetParam
- Formato de mídia do windows do método GetParam, interface IConfigAsfWriter2
- Formato de mídia da interface IConfigAsfWriter2 , método GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809136"
---
# <a name="iconfigasfwriter2getparam-method"></a>Método IConfigAsfWriter2::GetParam

O **método GetParam** recupera o valor atual do parâmetro de configuração de filtro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwParam* \[ Em\]
</dt> <dd>

Especifica o parâmetro a ser recuperado. Ele deve ser um valor definido na [ \_ \_ enumeração AM ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*pdwParam1* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recupera o valor do parâmetro especificado em *dwParam*.

</dd> <dt>

*pdwParam2* \[ out\]
</dt> <dd>

Não usado, deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 