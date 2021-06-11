---
description: Saiba mais sobre o método IAMFilterData::P arseFilterData, que desempacota os dados do Registro binário para um filtro. Essa interface foi substituída.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Método IAMFilterData::P arseFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989441"
---
# <a name="iamfilterdataparsefilterdata-method"></a>Método IAMFilterData::P arseFilterData

> [!Note]  
> Essa interface foi substituída. Novos aplicativos não devem usá-lo.

 

O `ParseFilterData` método desempacotará os dados do Registro binário para um filtro.

Normalmente, não há motivo para um aplicativo chamar esse método. O [**método IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornece uma maneira mais conveniente de acessar os dados do registro de filtro.

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

*rgbFilterData* \[ Em\]
</dt> <dd>

Ponteiro para os dados binários do Registro. Você pode obter esses dados recuperando a propriedade "FilterData" do moniker de filtro. Os dados são armazenados como **uma SAFEARRAY** de bytes (MATRIZ VT \_ UI1 \| \_ VT).

</dd> <dt>

*cb* \[ Em\]
</dt> <dd>

Especifica o tamanho dos dados binários, em bytes.

</dd> <dt>

*prgbRegFilter2* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para os dados desempacodados. Quando o método retornar, castirá-lo para um [**tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para acessar os dados de filtro. O chamador deve liberar a memória chamando o **método CoTaskMemFree.**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, retornará um código de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> O header Fil \_ data.h está localizado no diretório [Exemplo do Mapeador](mapper-sample.md) no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMFilterData Interface**](iamfilterdata.md)
</dt> </dl>

 

 




