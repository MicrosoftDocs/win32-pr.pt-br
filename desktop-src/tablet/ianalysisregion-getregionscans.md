---
description: Recupera uma matriz de retângulos que define a área do IAnalysisRegion.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Método IAnalysisRegion:: GetRegionScans (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779508"
---
# <a name="ianalysisregiongetregionscans-method"></a>Método IAnalysisRegion:: GetRegionScans

Recupera uma matriz de retângulos que define a área do [**IAnalysisRegion**](ianalysisregion.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulCount* \[ fora\]
</dt> <dd>

O número de retângulos retornados em *pRegionScans*.

</dd> <dt>

*pRegionScans* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de retângulos que define a área do [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se *pRegionScans* for passado como **NULL**, o método **GetRegionScans** retornará **S \_ OK** e o número de retângulos será retornado em *pulCount*.

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pRegionScans* quando você não precisar mais das informações.

 

Os limites dos retângulos estão em coordenadas de espaço de tinta.

A União dos retângulos retornados representa a área do [**IAnalysisRegion**](ianalysisregion.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como obter os retângulos que definem a área do [**IAnalysisRegion**](ianalysisregion.md) `region` e como obter apenas o número de retângulos.


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**Método IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

