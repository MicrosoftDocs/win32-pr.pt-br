---
description: Saiba mais sobre a interface IAMFilterData, que converte informações de filtro em dados binários empacotados. Essa interface foi substituída.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Interface IAMFilterData (Fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 9174549c93a76f94ccb7f039343a8eab5e75ece252871d11d60221df03aabe87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823596"
---
# <a name="iamfilterdata-interface"></a>Interface IAMFilterData

> [!Note]  
> Essa interface foi substituída. Os novos aplicativos devem usar a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) em vez disso.

 

A `IAMFilterData` interface converte informações de filtro em dados binários empacotados, que podem ser armazenados no registro. O objeto mapeador de filtro expõe essa interface.

## <a name="members"></a>Membros

A interface **IAMFilterData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMFilterData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAMFilterData** tem esses métodos.



| Método                                                     | Descrição                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Cria dados de registro binários para um filtro.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Desempacota os dados de registro binários de um filtro.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> o cabeçalho Fil \_ data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces preteridas](deprecated-interfaces.md)
</dt> </dl>

 

 
