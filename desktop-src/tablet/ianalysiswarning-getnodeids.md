---
description: Retorna os identificadores de todos os nós de contexto relevantes associados a este aviso.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Método IAnalysisWarning:: GetNodeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 97e6f4fde66faef14402c815f6b95517a2bd19adfb90eac4e865383770bc753f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967475"
---
# <a name="ianalysiswarninggetnodeids-method"></a>Método IAnalysisWarning:: GetNodeIds

Retorna os identificadores de todos os nós de contexto relevantes associados a este aviso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulCount* \[ entrada, saída\]
</dt> <dd>

O número de identificadores globalmente exclusivos (GUIDs) em *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de GUIDs que identifica os nós de contexto associados a esse aviso de análise, ou **NULL** se nenhum nó de contexto estiver associado ao aviso.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se *ppNodeIds* for passado como **NULL**, o método **GetNodeIds** retornará **S \_ OK** e o número de retângulos será retornado em *pulCount*.

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppNodeIds* quando você não precisar mais das informações.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como obter os objetos [**IContextNode**](icontextnode.md) que estão no [**IAnalysisWarning**](ianalysiswarning.md), `warning` e como obter apenas o número de objetos **IContextNode**


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

