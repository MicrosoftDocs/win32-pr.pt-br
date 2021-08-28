---
description: Adiciona dados de traço para vários traços a um nó de reconhecedor personalizado.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Método IInkAnalyzer:: AddStrokesToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9c50bcd1faa9df94847e3100309fc8598511dd760fa5efd6ccdf84812020fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719215"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>Método IInkAnalyzer:: AddStrokesToCustomRecognizer

Adiciona dados de traço para vários traços a um nó de reconhecedor personalizado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de traços a serem adicionados.

</dd> <dt>

*plStrokeIds* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de traço.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ no\]
</dt> <dd>

O número de propriedades em cada pacote.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de Propriedade do pacote.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ no\]
</dt> <dd>

Uma matriz que contém o número de pacotes em cada traço.

</dd> <dt>

*plStrokePacketData* \[ no\]
</dt> <dd>

Uma matriz que contém os dados de pacote para os traços.

</dd> <dt>

*pCustomRecognizer* \[ no\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** ao qual adicionar os traços.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ fora\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou os traços.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.

 

Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a um [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** (consulte [tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo aos traços e adiciona os traços ao primeiro nó **UnclassifiedInk** sob o nó **CustomRecognizer** . Se não existir nenhum nó **UnclassifiedInk** , ele será criado. Se o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associado ao nó **CustomRecognizer** não oferecer suporte ao identificador de cultura, o **IInkAnalyzer** continuará analisando e gera um aviso de [**IAnalysisWarning**](ianalysiswarning.md) . Esse aviso tem um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contém dados de pacote para todos os traços. *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada para o **método IInkAnalyzer:: AddStrokesToCustomRecognizer**.

 

Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora dos traços adicionados.

O [**IInkAnalyzer**](iinkanalyzer.md) retorna um **HRESULT** de **E \_ INVALIDARG** sob as circunstâncias a seguir.

-   O [**IInkAnalyzer**](iinkanalyzer.md) já contém um traço com o mesmo identificador de um dos traços a serem adicionados.
-   O parâmetro *pCustomRecognizer* contém um nó de reconhecedor personalizado que está associado a um objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   O parâmetro *pCustomRecognizer* contém um [**IContextNode**](icontextnode.md) que não é do tipo **CustomRecognizer**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

