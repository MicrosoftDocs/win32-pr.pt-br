---
description: Adiciona dados de traço para um único traço a um nó de reconhecedor personalizado.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: Método IInkAnalyzer::AddRogkeToCustomRecognizer (IACom.h)
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
ms.openlocfilehash: 0a3ce58f462053b48e6cecdc7eb276a1e162f88b0e7de373648a537b3b712cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967325"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Método IInkAnalyzer::AddRogkeToCustomRecognizer

Adiciona dados de traço para um único traço a um nó de reconhecedor personalizado.

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

*ulStrkeId* \[ Em\]
</dt> <dd>

O identificador do traço a ser acrescentado.

</dd> <dt>

*ulRogkePacketDataCount* \[ Em\]
</dt> <dd>

O número de pacotes no traço.

</dd> <dt>

*plRogkePacketData* \[ Em\]
</dt> <dd>

Uma matriz que contém os dados de pacote para o traço.

</dd> <dt>

*ulRogkePacketDescriptionCount* \[ Em\]
</dt> <dd>

O número de propriedades de pacote em cada pacote.

</dd> <dt>

*pRogkePacketDescriptionGuids* \[ Em\]
</dt> <dd>

Uma matriz que contém os identificadores de propriedade do pacote.

</dd> <dt>

*pCustomRecognizer* \[ Em\]
</dt> <dd>

O [**IContextNode do**](icontextnode.md) tipo **CustomRecognizer** ao qual adicionar o traço.

</dd> <dt>

*ppContextNodeStrkeAddedTo* \[ out\]
</dt> <dd>

O [**IContextNode ao**](icontextnode.md) qual o analisador de tinta adicionou o traço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrkeAddedTo* quando você não precisar mais usar o objeto .

 

Quando *ppContextNodeStrkeAddedTo* é **NULL**, indica que o chamador não está interessado no valor de retorno do método .

O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a [**um IContextNode**](icontextnode.md) do tipo **CustomRecognizer** (consulte [Tipos de nó de contexto](context-node-types.md)). Esse nó está na coleção de subnodos do nó raiz (consulte Métodos [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro **nó UnclassifiedInk** sob o **nó CustomRecognizer.** Se nenhum **nó UnclassifiedInk** existir, ele será criado. Se [**o IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associado ao nó **CustomRecognizer** não dá suporte ao identificador de cultura, o **IInkAnalyzer** continua analisando e gera um aviso [**IAnalysisWarning.**](ianalysiswarning.md) Este aviso tem um [**valor AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **de AnalysisWarningCode \_ LanguageIdNotRespected**.

*plRogkePacketData* contém dados de pacote para todos os pontos no traço. *pRogkePacketDescriptionGuids* contém os GUIDs (identificadores globalmente exclusivos) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para ver uma lista completa das propriedades de pacote disponíveis, consulte [Constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Esse método expande a região suja para a união do valor atual da região e a caixa delimitativa do traço adicionado.

O [**IInkAnalyzer**](iinkanalyzer.md) retorna um **HRESULT** de **E \_ INVALIDARG** nas circunstâncias a seguir.

-   O [**IInkAnalyzer**](iinkanalyzer.md) já contém um traço com o mesmo identificador que o traço a ser adicionado.
-   O *parâmetro pCustomRecognizer* contém um nó de reconhecedor personalizado associado a um objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   O *parâmetro pCustomRecognizer* contém [**um IContextNode**](icontextnode.md) que não é do tipo **CustomRecognizer.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[**Método IInkAnalyzer::AddRogkesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer::CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

