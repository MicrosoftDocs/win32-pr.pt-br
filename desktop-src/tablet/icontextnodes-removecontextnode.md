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
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762500"
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

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




