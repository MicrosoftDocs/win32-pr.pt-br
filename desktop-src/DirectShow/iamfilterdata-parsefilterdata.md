---
description: Observe que essa interface foi preterida.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData: método arseFilterData de:P (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768643"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData: método arseFilterData de:P

> [!Note]  
> Essa interface foi substituída. Novos aplicativos não devem usá-lo.

 

O `ParseFilterData` método desempacota os dados de registro binários para um filtro.

Normalmente, não há motivo para um aplicativo chamar esse método. O método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornece uma maneira mais conveniente de acessar os dados do registro de filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rgbFilterData* \[ no\]
</dt> <dd>

Ponteiro para os dados do registro binário. Você pode obter esses dados recuperando a propriedade "FilterData" do moniker do filtro. Os dados são armazenados como um **SafeArray** de bytes ( \_ matriz VT UI1 \| VT \_ ).

</dd> <dt>

*CB* \[ no\]
</dt> <dd>

Especifica o tamanho dos dados binários, em bytes.

</dd> <dt>

*prgbRegFilter2* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para os dados desempacotados. Quando o método retorna, converta esse ponteiro para um tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para acessar os dados de filtro. O chamador deve liberar a memória chamando o método **CoTaskMemFree** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, retornará um código de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




