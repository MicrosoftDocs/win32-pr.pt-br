---
description: Remove um objeto IContextNode desta coleção.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'Método IContextNodes:: RemoveContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8fa1fd222e671dfd87f15862108ea66df3b99e530d453cf4614b7572d31b275c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092297"
---
# <a name="icontextnodesremovecontextnode-method"></a>Método IContextNodes:: RemoveContextNode

Remove um objeto [**IContextNode**](icontextnode.md) desta coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextNode* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




