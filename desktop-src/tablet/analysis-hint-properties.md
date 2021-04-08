---
description: 'Define identificadores globais exclusivos (GUIDs) para propriedades de um nó de dica de análise (consulte IContextNode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propriedades da dica de análise (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920619"
---
# <a name="analysis-hint-properties"></a>Propriedades da dica de análise

Define identificadores globais exclusivos (GUIDs) para propriedades de um nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).

A tabela a seguir descreve as informações referenciadas por cada constante.



| Constante                                                                                                                                                                                                                                  | Descrição                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt> </dl>       | Se termos de dicionário parciais são permitidos em uma dica de análise.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt> </dl>                                        | O nome de uma dica de análise.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt> </dl>                                           | Se o analisador de tinta limita sua análise de tinta na área da dica para estar de acordo com o factor.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt> </dl> | A dica contém uma matriz de caracteres que representa o conjunto restrito de conjunto de caracteres Unicode com suporte permitido por este InkRecognizer.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**\_factor de AHP GUID \_**</dt> </dl>                                                                   | O factor em uma dica de análise.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**\_Guia de AHP GUID \_**</dt> </dl>                                                                         | A estrutura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) que representa o guia para uma dica de análise.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PREFIXTEXT**</dt> </dl>                                                          | O texto do prefixo em uma dica de análise.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt> </dl>                                                          | O texto do sufixo em uma dica de análise.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt> </dl>                                        | Se as várias segmentações nos resultados do reconhecimento de tinta estão desabilitadas.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**\_AHP de \_ palavras de GUID**</dt> </dl>                                                                | A matriz de cadeias de caracteres que representa a lista de palavras para uma dica de análise.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ AHP \_ WordMode**</dt> </dl>                                                                | Se o analisador de tinta prioriza resultados de palavras únicas em resultados de várias palavras para uma dica de análise.<br/>                                      |



## <a name="remarks"></a>Comentários

Essas GUIDs são usadas para identificar propriedades que o [**IInkAnalyzer**](iinkanalyzer.md) pode definir em um nó de contexto de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).

Para obter ou definir propriedades de um [**IContextNode**](icontextnode.md) em geral, consulte [Propriedades do nó de contexto](context-node-properties.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades do nó de contexto](context-node-properties.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




