---
description: Adiciona um novo nó de dica de análise com uma área infinita ao IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Método IInkAnalyzer:: CreateAnalysisHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296390"
---
# <a name="iinkanalyzercreateanalysishint-method"></a>Método IInkAnalyzer:: CreateAnalysisHint

Adiciona um novo nó de dica de análise com uma área infinita ao [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAnalysisHint* \[ fora\]
</dt> <dd>

O novo nó de dica de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md) para obter uma descrição dos valores de retorno.

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAnalysisHint* quando você não precisar mais usar o objeto.

 

Para fornecer informações adicionais de contexto para o [**IInkAnalyzer**](iinkanalyzer.md), você pode adicionar dicas de análise ao analisador de tinta. As dicas de análise podem melhorar a precisão do reconhecimento. Por exemplo, você pode adicionar informações de factor e de guia para campos em um aplicativo de formulário.

Esse método cria um novo [**IContextNode**](icontextnode.md) com um tipo de nó de contexto AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) e adiciona a nova dica como um subnó do nó raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o método [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).

Para adicionar informações de contexto à dica, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) com o parâmetro *pPropertyDataId* definido como uma das constantes de [Propriedades de dica de análise](analysis-hint-properties.md) .

Se uma dica for atribuída a uma área infinita, com o termo de uma dica global, o [**IInkAnalyzer**](iinkanalyzer.md) aplicará o contexto da dica a toda a tinta que não está dentro da área de outra dica. Várias dicas podem ser anexadas a um único **IInkAnalyzer**. No entanto, apenas uma dica global pode ser anexada a um único analisador de tinta e não há dicas globais que podem se sobrepor. Para obter mais informações sobre os tipos de informações de contexto que podem ser fornecidas por uma dica, consulte [Propriedades de dica de análise](analysis-hint-properties.md).

A adição de uma dica de análise não marca a área da dica para reanálise. Para marcar a área dentro da dica para reanálise, use o [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para definir a região suja como a União da região suja atual e da área da dica de análise.

Ao usar dicas para um aplicativo de formulário, o aplicativo deve evitar misturar o contexto de texto com tinta nos formulários. Isso significa, por exemplo, que os nomes de campo de texto não devem ser criados na árvore de análise. As dicas destinam-se a associar a tinta a áreas em páginas; qualquer contexto de texto interfere nessa associação de tinta para dica. A operação de análise pode mesclar a tinta e o contexto de texto na mesma região de escrita, o que impediria que a tinta fosse associada à área de dica.

Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).

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

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IInkAnalyzer: método eleteAnalysisHint de:D**](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Propriedades da dica de análise](analysis-hint-properties.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

