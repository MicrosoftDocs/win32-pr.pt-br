---
description: Recupera uma matriz de identificadores para os traços dentro do objeto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: Método IContextNode::GetRogkeIds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ebe66d514b20fc558adce39c013cf559fbc63bb38f772bff73b0819c10426960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967365"
---
# <a name="icontextnodegetstrokeids-method"></a>Método IContextNode::GetStrkeIds

Recupera uma matriz de identificadores para os traços dentro do [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

O número de traços. O valor passado não é usado.

</dd> <dt>

*pplStrkes* \[ out\]
</dt> <dd>

Um ponteiro para a matriz de identificadores de traço para este [**objeto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória de \* *pplStrkes* quando você não precisar mais das informações.

 

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

[**IContextNode::GetRogkeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**IContextNode::GetRogkeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

