---
description: Define identificadores globais exclusivos (GUIDs) para propriedades de um IContextNode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Propriedades do nó de contexto (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826715"
---
# <a name="context-node-properties"></a>Propriedades do nó de contexto

Define identificadores globais exclusivos (GUIDs) para propriedades de um [**IContextNode**](icontextnode.md).

A tabela a seguir descreve as informações referenciadas por cada constante.



| Constante                                                                                                                                                                                                 | Descrição                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt> </dl>             | O nível de alinhamento de um parágrafo.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ CNP \_ ascendentes**</dt> </dl>                            | Os ascendentes de uma palavra à tinta.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**\_linha de \_ base CNP GUID**</dt> </dl>                               | A linha de base de uma palavra de tinta.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt> </dl>          | O nível de confiança nos resultados do reconhecimento.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt> </dl> | O identificador do reconhecedor de tinta personalizado para um nó de reconhecedor personalizado.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**GUID \_ CNP \_ descendentes**</dt> </dl>                         | Os descendentes de uma palavra à tinta.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ CNP \_ Tabs no meio**</dt> </dl>                                  | O Tabs no meio de uma palavra de tinta.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ NODEDATA**</dt> </dl>                               | Os dados de imagem ou dados de texto de uma imagem ou uma palavra de texto.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ reconhecívelstring**</dt> </dl>       | A cadeia de caracteres reconhecida.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt> </dl> | A caixa delimitadora girada.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**\_CNP \_ semânticatype de GUID**</dt> </dl>                   | A propriedade contém informações sobre os tipos semânticos usados na definição de uma anotação, como se é um texto explicativo, um comentário e assim por diante.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ FormatName**</dt> </dl>                            | O nome da forma de um nó de desenho de tinta.<br/>                                                                                                            |



## <a name="remarks"></a>Comentários

Essas GUIDs são usadas para identificar propriedades que o [**IInkAnalyzer**](iinkanalyzer.md) pode definir em um [**IContextNode**](icontextnode.md). O analisador de tinta define alguns dados de propriedade com base no tipo do nó de contexto (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).

Para obter ou definir propriedades específicas para nós de dica de análise, consulte [**Propriedades de dica de análise**](analysis-hint-properties.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da dica de análise](analysis-hint-properties.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
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

 

 




