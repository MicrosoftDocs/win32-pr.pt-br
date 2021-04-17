---
description: Atualiza os dados de pacote para os traços especificados.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Método IInkAnalyzer:: UpdateStrokesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762439"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>Método IInkAnalyzer:: UpdateStrokesData

Atualiza os dados de pacote para os traços especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de traços a serem atualizados.

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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

o parâmetro *plStrokePacketData* contém dados de pacote para todos os traços. O parâmetro *pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

Somente traços com as mesmas descrições de pacote podem ser atualizados em uma única chamada para o **método IInkAnalyzer:: UpdateStrokesData**.

Esse método não atualiza a região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Se um traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.

Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.

Esse método retorna um código de erro quando *plStrokeIds* é **nulo**.

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

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




