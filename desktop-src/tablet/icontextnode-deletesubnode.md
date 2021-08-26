---
description: Remove um IContextNode filho.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: Método IContextNode::D eleteSubNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0ebad42f02ccfad0db2d119832f3495819ac18ce321d72ede3aa8d7545b999be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057876"
---
# <a name="icontextnodedeletesubnode-method"></a>Método IContextNode::D eleteSubNode

Remove um [**IContextNode filho.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextNodeToDelete* \[ Em\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

E \_ INVALIDARG será retornado se o *parâmetro pContextNodeToDelete* não for um filho desse [**objeto IContextNode.**](icontextnode.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




