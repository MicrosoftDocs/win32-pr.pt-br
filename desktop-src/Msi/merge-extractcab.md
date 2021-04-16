---
description: O método ExtractCAB do objeto de mesclagem extrai o arquivo. cab inserido de um módulo e o salva como o arquivo especificado. O instalador criará esse arquivo se ele ainda não existir e substituído se ele existir.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Método Merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758304"
---
# <a name="mergeextractcab-method"></a>Método Merge. ExtractCAB

O método **ExtractCAB** do objeto de [**mesclagem**](merge-object.md) extrai o arquivo. cab inserido de um módulo e o salva como o arquivo especificado. O instalador criará esse arquivo se ele ainda não existir e substituído se ele existir.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* 
</dt> <dd>

O arquivo de destino totalmente qualificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="c"></a>C++

Consulte a função [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
