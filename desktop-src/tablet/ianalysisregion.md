---
description: Expõe métodos e propriedades para uma região que representa uma área de um documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interface IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647239"
---
# <a name="ianalysisregion-interface"></a>Interface IAnalysisRegion

Expõe métodos e propriedades para uma região que representa uma área de um documento.

## <a name="members"></a>Membros

A interface **IAnalysisRegion** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisRegion** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAnalysisRegion** tem esses métodos.



| Método                                                           | Descrição                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**8i**](ianalysisregion-clone.md)                           | Cria uma cópia do **IAnalysisRegion**.<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Restringe a área do **IAnalysisRegion** à parte de sua área que não faz a interseção do retângulo especificado.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Restringe a área do **IAnalysisRegion** à parte de sua área que não faz a interseção do **IAnalysisRegion** especificado.<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Recupera o retângulo delimitador do **IAnalysisRegion**.<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Recupera uma matriz de retângulos que define a área do **IAnalysisRegion**.<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Restringe a área desta **IAnalysisRegion** para a área criada por sua interseção com o retângulo especificado.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Restringe a área de **IAnalysisRegion** para a área criada por sua interseção com o **IAnalysisRegion** especificado.<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Determina se a área do **IAnalysisRegion** intersecciona com o retângulo especificado.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Recupera um valor que indica se **IAnalysisRegion** representa uma região vazia.<br/>                                            |
| [**IsFinite**](ianalysisregion-isinfinite.md)                 | Recupera um valor que indica se **IAnalysisRegion** representa uma região infinita.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Reduz o **IAnalysisRegion** para representar uma área vazia.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Expande o **IAnalysisRegion** para representar uma área infinita.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Expande a área desta **IAnalysisRegion** para a área criada por sua união com o retângulo especificado.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Expande a área desta **IAnalysisRegion** para a área criada por sua união com o **IAnalysisRegion** especificado.<br/>               |



 

## <a name="remarks"></a>Comentários

Essa interface representa uma área que é construída a partir de regiões retangulares. O [**IInkAnalyzer**](iinkanalyzer.md) retorna ou interpreta as coordenadas de uma área dentro do espaço de coordenadas no qual recebe dados de traço.

Para obter os limites atuais do **IAnalysisRegion**, use o método [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) ou o [**método IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).

Para modificar a área de um **IAnalysisRegion** existente, use os métodos a seguir.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**Método IAnalysisRegion:: ExcludeRegion**](ianalysisregion-excluderegion.md)
-   [**Método IAnalysisRegion:: IntersectRectangle**](ianalysisregion-intersectrectangle.md)
-   [**Método IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
-   [**Método IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
-   [**Método IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
-   [**Método IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
-   [**Método IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)

Essa interface é equivalente à classe System. Windows. Ink. AnalysisCore. AnalysisRegionBase na .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

