---
description: Adiciona dados de traço para um único traço para um nó de reconhecedor personalizado.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Método IInkAnalyzer:: AddStrokeToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772538"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Método IInkAnalyzer:: AddStrokeToCustomRecognizer

Adiciona dados de traço para um único traço para um nó de reconhecedor personalizado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeId* \[ no\]
</dt> <dd>

O identificador do traço a ser adicionado.

</dd> <dt>

*ulStrokePacketDataCount* \[ no\]
</dt> <dd>

O número de pacotes no traço.

</dd> <dt>

*plStrokePacketData* \[ no\]
</dt> <dd>

Uma matriz que contém os dados de pacote para o traço.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ no\]
</dt> <dd>

O número de propriedades do pacote em cada pacote.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ no\]
</dt> <dd>

Uma matriz que contém os identificadores de Propriedade do pacote.

</dd> <dt>

*pCustomRecognizer* \[ no\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** ao qual adicionar o traço.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ fora\]
</dt> <dd>

O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou o traço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.

 

Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a um [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** (consulte [tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro nó **UnclassifiedInk** sob o nó **CustomRecognizer** . Se não existir nenhum nó **UnclassifiedInk** , ele será criado. Se o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associado ao nó **CustomRecognizer** não oferecer suporte ao identificador de cultura, o **IInkAnalyzer** continuará analisando e gera um aviso de [**IAnalysisWarning**](ianalysiswarning.md) . Esse aviso tem um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contém dados de pacote para todos os pontos no traço. *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora do traço adicionado.

O [**IInkAnalyzer**](iinkanalyzer.md) retorna um **HRESULT** de **E \_ INVALIDARG** sob as circunstâncias a seguir.

-   O [**IInkAnalyzer**](iinkanalyzer.md) já contém um traço com o mesmo identificador que o traço a ser adicionado.
-   O parâmetro *pCustomRecognizer* contém um nó de reconhecedor personalizado que está associado a um objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   O parâmetro *pCustomRecognizer* contém um [**IContextNode**](icontextnode.md) que não é do tipo **CustomRecognizer**.

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

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

