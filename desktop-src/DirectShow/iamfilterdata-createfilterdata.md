---
description: 'Saiba mais sobre o método IAMFilterData:: CreateFilterData, que cria dados de registro binários para um filtro. Essa interface foi substituída.'
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Método IAMFilterData:: CreateFilterData (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 81c2ba3a56ba9c09a2ce7b23bcad1a83880e61256402c291b5aebde9988218c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428666"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>Método IAMFilterData:: CreateFilterData

> [!Note]  
> Essa interface foi substituída. Novos aplicativos não devem usá-lo.

 

O `CreateFilterData` método cria dados de registro binários para um filtro. Esses dados podem ser gravados no registro como uma \_ subchave binária reg chamada FilterData, na chave CLSID do filtro.

Normalmente, não há motivo para um aplicativo chamar esse método. O método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) cria automaticamente os dados binários e os adiciona ao local correto no registro. para obter mais informações, consulte [como registrar filtros de DirectShow](how-to-register-directshow-filters.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prf2* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contém as informações de filtro.

</dd> <dt>

*prgbFilterData* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para os dados binários. O método aloca a memória para os dados. O chamador deve liberar a memória chamando o método **CoTaskMemFree** .

</dd> <dt>

*PCB* \[ fora\]
</dt> <dd>

Ponteiro para uma variável que recebe o tamanho dos dados binários, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, ele retornará S \_ OK. Se falhar, retornará um código de erro.

## <a name="remarks"></a>Comentários

> [!Note]  
> o cabeçalho Fil \_ data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




