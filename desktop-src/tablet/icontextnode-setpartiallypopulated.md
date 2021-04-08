---
description: Modifica o valor que indica se este IContextNode está parcialmente ou totalmente preenchido.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Método IContextNode:: SetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010524"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>Método IContextNode:: SetPartiallyPopulated

Modifica o valor que indica se este [**IContextNode**](icontextnode.md) está parcialmente ou totalmente preenchido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fPartiallyPopulated* \[ no\]
</dt> <dd>

**Variante \_ TRUE** se este [**IContextNode**](icontextnode.md) for parcialmente preenchido; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Para obter mais informações, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

Ao virtualizar sua árvore de documentos, certifique-se de definir o valor PropertyGuidsForContextNodes. RotatedBoundingBox (usando ContextNode. addpropertyvalue) em todos os objetos ContextNode. A propriedade RotatedBoundingBox é calculada pelo InkAnalyzer e, por padrão, deve estar em todos os ContextNodes de gravação. No entanto, se seu aplicativo virtualiza os resultados da análise definindo a propriedade PartiallyPopulated, ao manipular o evento PopulateContextNode, certifique-se de preencher a propriedade RotatedBoundingBox. Falha ao definir a propriedade RotatedBoundingBox resultará em potencialmente mais dados de documento sendo usados na operação de análise atual

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




