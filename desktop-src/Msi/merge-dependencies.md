---
description: A propriedade de dependências somente leitura do objeto de mesclagem retorna uma coleção de objetos de dependência que enumera um conjunto de dependências não atendidas para o banco de dados atual.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Propriedade Merge. Dependencies (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750608"
---
# <a name="mergedependencies-property"></a>Propriedade Merge. Dependencies

A propriedade de **dependências** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção de objetos de [**dependência**](dependency-object.md) que enumera um conjunto de dependências não atendidas para o banco de dados atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Um módulo não precisa estar aberto para recuperar informações de dependência.

### <a name="c"></a>C++

Consulte a função [**obter \_ dependências**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
