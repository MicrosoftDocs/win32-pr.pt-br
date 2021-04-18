---
description: Observe que essa interface foi preterida.
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
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759125"
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
> O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces preteridas](deprecated-interfaces.md)
</dt> </dl>

 

 
