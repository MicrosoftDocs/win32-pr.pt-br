---
title: Identificadores de tipo de anotação (UIAutomationClient. h)
description: Este tópico descreve as constantes nomeadas que são usadas para identificar tipos de anotações em um documento.
ms.assetid: 46948B7C-EC9F-4B55-B769-62EE8BE11D33
topic_type:
- apiref
api_name:
- AnnotationType_AdvancedProofingIssue
- AnnotationType_Author
- AnnotationType_CircularReferenceError
- AnnotationType_Comment
- AnnotationType_ConflictingChange
- AnnotationType_DataValidationError
- AnnotationType_DeletionChange
- AnnotationType_EditingLockedChange
- AnnotationType_Endnote
- AnnotationType_ExternalChange
- AnnotationType_Footer
- AnnotationType_Footnote
- AnnotationType_FormatChange
- AnnotationType_FormulaError
- AnnotationType_GrammarError
- AnnotationType_Header
- AnnotationType_Highlighted
- AnnotationType_InsertionChange
- AnnotationType_Mathematics
- AnnotationType_MoveChange
- AnnotationType_SpellingError
- AnnotationType_TrackChanges
- AnnotationType_Unknown
- AnnotationType_UnsyncedChange
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb628c8e6ada93546291cd9afb87c3194798b9f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644202"
---
# <a name="annotation-type-identifiers"></a>Identificadores de tipo de anotação

Este tópico descreve as constantes nomeadas que são usadas para identificar tipos de anotações em um documento.



| Constante/valor                                                                                                                                                                                                                                                                                                                                           | Description                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span id="AnnotationType_AdvancedProofingIssue"></span><span id="annotationtype_advancedproofingissue"></span><span id="ANNOTATIONTYPE_ADVANCEDPROOFINGISSUE"></span><dl> <dt>**\_ AnnotationType AdvancedProofingIssue**</dt> <dt>60020</dt> </dl>     | Um problema de prova avançada.<br/>                                                             |
| <span id="AnnotationType_Author"></span><span id="annotationtype_author"></span><span id="ANNOTATIONTYPE_AUTHOR"></span><dl> <dt>**\_ AnnotationType Autor**</dt> <dt>60019</dt> </dl>                                                                 | O autor do documento.<br/>                                                             |
| <span id="AnnotationType_CircularReferenceError"></span><span id="annotationtype_circularreferenceerror"></span><span id="ANNOTATIONTYPE_CIRCULARREFERENCEERROR"></span><dl> <dt>**\_ AnnotationType CircularReferenceError**</dt> <dt>60022</dt> </dl> | Um erro de referência circular que ocorreu.<br/>                                               |
| <span id="AnnotationType_Comment"></span><span id="annotationtype_comment"></span><span id="ANNOTATIONTYPE_COMMENT"></span><dl> <dt>**\_ AnnotationType Comentário**</dt> <dt>60003</dt> </dl>                                                             | Um comentário. Os comentários podem assumir diferentes formas dependendo do aplicativo.<br/>              |
| <span id="AnnotationType_ConflictingChange"></span><span id="annotationtype_conflictingchange"></span><span id="ANNOTATIONTYPE_CONFLICTINGCHANGE"></span><dl> <dt>**\_ AnnotationType ConflictingChange**</dt> <dt>60018</dt> </dl>                     | Uma alteração conflitante que foi feita no documento.<br/>                                     |
| <span id="AnnotationType_DataValidationError"></span><span id="annotationtype_datavalidationerror"></span><span id="ANNOTATIONTYPE_DATAVALIDATIONERROR"></span><dl> <dt>**\_ AnnotationType Datavalidationerror**</dt> <dt>60021</dt> </dl>             | Um erro de validação de dados que ocorreu.<br/>                                                  |
| <span id="AnnotationType_DeletionChange"></span><span id="annotationtype_deletionchange"></span><span id="ANNOTATIONTYPE_DELETIONCHANGE"></span><dl> <dt>**\_ AnnotationType DeletionChange**</dt> <dt>60012</dt> </dl>                                 | Uma alteração de exclusão feita no documento.<br/>                                        |
| <span id="AnnotationType_EditingLockedChange"></span><span id="annotationtype_editinglockedchange"></span><span id="ANNOTATIONTYPE_EDITINGLOCKEDCHANGE"></span><dl> <dt>**\_ AnnotationType EditingLockedChange**</dt> <dt>60016</dt> </dl>             | Uma alteração bloqueada de edição que foi feita no documento.<br/>                                 |
| <span id="AnnotationType_Endnote"></span><span id="annotationtype_endnote"></span><span id="ANNOTATIONTYPE_ENDNOTE"></span><dl> <dt>**\_ AnnotationType Nota de fim**</dt> <dt>60009</dt> </dl>                                                             | A nota de fim de um documento.<br/>                                                             |
| <span id="AnnotationType_ExternalChange"></span><span id="annotationtype_externalchange"></span><span id="ANNOTATIONTYPE_EXTERNALCHANGE"></span><dl> <dt>**\_ AnnotationType ExternalChange**</dt> <dt>60017</dt> </dl>                                 | Uma alteração externa que foi feita no documento.<br/>                                       |
| <span id="AnnotationType_Footer"></span><span id="annotationtype_footer"></span><span id="ANNOTATIONTYPE_FOOTER"></span><dl> <dt>**\_ AnnotationType Rodapé**</dt> <dt>60007</dt> </dl>                                                                 | O rodapé de uma página em um documento.<br/>                                                    |
| <span id="AnnotationType_Footnote"></span><span id="annotationtype_footnote"></span><span id="ANNOTATIONTYPE_FOOTNOTE"></span><dl> <dt>**\_ AnnotationType Nota de rodapé**</dt> <dt>60010</dt> </dl>                                                         | A nota de rodapé de uma página em um documento.<br/>                                                  |
| <span id="AnnotationType_FormatChange"></span><span id="annotationtype_formatchange"></span><span id="ANNOTATIONTYPE_FORMATCHANGE"></span><dl> <dt>**\_ AnnotationType FormatChange**</dt> <dt>60014</dt> </dl>                                         | Uma alteração de formato feita.<br/>                                                          |
| <span id="AnnotationType_FormulaError"></span><span id="annotationtype_formulaerror"></span><span id="ANNOTATIONTYPE_FORMULAERROR"></span><dl> <dt>**\_ AnnotationType FormulaError**</dt> <dt>60004</dt> </dl>                                         | Um erro em uma fórmula. Os erros de fórmula normalmente incluem texto vermelho e pontos de exclamação.<br/> |
| <span id="AnnotationType_GrammarError"></span><span id="annotationtype_grammarerror"></span><span id="ANNOTATIONTYPE_GRAMMARERROR"></span><dl> <dt>**\_ AnnotationType GrammarError**</dt> <dt>60002</dt> </dl>                                         | Um erro gramatical, geralmente indicado por uma linha ondulada verde. <br/>                           |
| <span id="AnnotationType_Header"></span><span id="annotationtype_header"></span><span id="ANNOTATIONTYPE_HEADER"></span><dl> <dt>**\_ AnnotationType Cabeçalho**</dt> <dt>60006</dt> </dl>                                                                 | O cabeçalho de uma página em um documento.<br/>                                                    |
| <span id="AnnotationType_Highlighted"></span><span id="annotationtype_highlighted"></span><span id="ANNOTATIONTYPE_HIGHLIGHTED"></span><dl> <dt>**\_ AnnotationType Realçado**</dt> <dt>60008</dt> </dl>                                             | Conteúdo realçado, normalmente indicado por uma cor de fundo de contraste.<br/>               |
| <span id="AnnotationType_InsertionChange"></span><span id="annotationtype_insertionchange"></span><span id="ANNOTATIONTYPE_INSERTIONCHANGE"></span><dl> <dt>**\_ AnnotationType InsertionChange**</dt> <dt>60011</dt> </dl>                             | Uma alteração de inserção feita no documento.<br/>                                      |
| <span id="AnnotationType_Mathematics"></span><span id="annotationtype_mathematics"></span><span id="ANNOTATIONTYPE_MATHEMATICS"></span><dl> <dt>**\_ AnnotationType Matemática**</dt> <dt>60023</dt> </dl>                                             | Um intervalo de texto contendo matemática.<br/>                                                    |
| <span id="AnnotationType_MoveChange"></span><span id="annotationtype_movechange"></span><span id="ANNOTATIONTYPE_MOVECHANGE"></span><dl> <dt>**\_ AnnotationType MoveChange**</dt> <dt>60013</dt> </dl>                                                 | Uma alteração de movimentação feita no documento.<br/>                                            |
| <span id="AnnotationType_SpellingError"></span><span id="annotationtype_spellingerror"></span><span id="ANNOTATIONTYPE_SPELLINGERROR"></span><dl> <dt>**\_ AnnotationType SpellingError**</dt> <dt>60001</dt> </dl>                                     | Um erro de ortografia, geralmente indicado por uma linha ondulada vermelha. <br/>                                |
| <span id="AnnotationType_TrackChanges"></span><span id="annotationtype_trackchanges"></span><span id="ANNOTATIONTYPE_TRACKCHANGES"></span><dl> <dt>**\_ AnnotationType TrackChanges**</dt> <dt>60005</dt> </dl>                                         | Uma alteração feita no documento.<br/>                                                 |
| <span id="AnnotationType_Unknown"></span><span id="annotationtype_unknown"></span><span id="ANNOTATIONTYPE_UNKNOWN"></span><dl> <dt>**\_ AnnotationType**</dt> <dt>60000</dt> desconhecido </dl>                                                             | O tipo de anotação é desconhecido.<br/>                                                         |
| <span id="AnnotationType_UnsyncedChange"></span><span id="annotationtype_unsyncedchange"></span><span id="ANNOTATIONTYPE_UNSYNCEDCHANGE"></span><dl> <dt>**\_ AnnotationType UnsyncedChange**</dt> <dt>60015</dt> </dl>                                 | Uma alteração não sincronizada que foi feita no documento.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                            |
| parâmetro<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**IAnnotationProvider::AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)
</dt> <dt>

[**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)
</dt> <dt>

[**IUIAutomationPattern::CachedAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_cachedannotationtypeid)
</dt> <dt>

[**IUIAutomationPattern::CurrentAnnotationTypeId**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationannotationpattern-get_currentannotationtypeid)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes)
</dt> <dt>

[**IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationType**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>

 

