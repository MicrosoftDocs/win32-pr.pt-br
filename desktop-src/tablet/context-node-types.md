---
description: Essas constantes definem valores que especificam o tipo de objetos IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipos de nó de contexto (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 2bb2064cc72b398d290fa78606b31bd37208535e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473882"
---
# <a name="context-node-types"></a>Tipos de nó de contexto

Essas constantes definem valores que especificam o tipo de objetos [**IContextNode**](icontextnode.md) .




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt><dt>(ANALYSISHINT)</dt></dl> | Representa um nó que contém informações adicionais de contexto para uma região que o <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> usa para melhorar sua análise.<br /> | 
| <span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt><dt>(CUSTOMRECOGNIZER)</dt></dl> | Representa um nó usado para uma única operação de reconhecimento.<br /> Todos os traços e nós que estão dentro de um nó de reconhecedor personalizado são reconhecidos por uma operação de reconhecimento independente e não são analisados pelo <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.<br /> Um nó de reconhecedor personalizado deve ser o filho direto do nó raiz do analisador de tinta.<br /> Um nó de reconhecedor personalizado pode conter os seguintes tipos de elementos filho:<br /><ul><li>Qualquer número de nós UnclassifiedInk.</li><li>Qualquer número de nós de objeto.</li><li>Qualquer número de nós de linha.</li><li>Qualquer número de nós InkWord.</li><li>Qualquer número de nós com um valor de GUID desconhecido.</li></ul> | 
| <span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl><dt><strong>GUID_CNT_IMAGE</strong></dt><dt>(imagem)</dt></dl> | Representa um nó para uma região bidimensional em que qualquer imagem que não seja de tinta pode existir no documento.<br /> O <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> não produz nós de imagem. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para adicionar um nó de imagem à árvore de nós de contexto. Em seguida, o <strong>IInkAnalyzer</strong> usa as regiões definidas pelo nó de imagem para determinar se alguma tinta anota a imagem que não é de tinta.<br /> Um nó de imagem não pode ter nenhum elemento filho.<br /> | 
| <span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl><dt><strong>GUID_CNT_INKBULLET</strong></dt><dt>(INKBULLET)</dt></dl> | O InkBullet ContextNodeType representa uma coleção de traços que compõem um marcador em uma lista com marcadores.<br /> Um ContextNode do tipo InkBullet não pode ter filhos. Só pode ser um filho de um parágrafo ContextNode. Somente um InkBullet pode aparecer em um único parágrafo ContextNode.<br /> | 
| <span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl><dt><strong>GUID_CNT_INKDRAWING</strong></dt><dt>(INKDRAWING)</dt></dl> | Representa um nó para uma coleção de traços que constitui um desenho.<br /> Os desenhos são traços que são determinados como formas ou esboços abstratos. Geralmente, eles são traços que não são classificados como traços de escrita.<br /> Um nó de desenho de tinta não pode ter nenhum elemento filho.<br /> | 
| <span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl><dt><strong>GUID_CNT_INKWORD</strong></dt><dt>(INKWORD)</dt></dl> | Representa um nó para uma coleção de traços que constitui um agrupamento lógico para formar uma palavra reconhecível.<br /> Um nó de palavra à tinta não pode conter nenhum elemento filho.<br /> | 
| <span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl><dt><strong>GUID_CNT_LINE</strong></dt><dt>(linha)</dt></dl> | Representa um nó para uma linha de palavras.<br /> Um nó de linha pode conter os seguintes tipos de elementos filho:<br /><ul><li>Qualquer número de nós de palavras de tinta.</li><li>Qualquer número de nós da palavra de texto.</li><li>Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</li></ul> | 
| <span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl><dt><strong>GUID_CNT_OBJECT</strong></dt><dt>(objeto)</dt></dl> | Representa um nó para um objeto que é retornado de um reconhecedor personalizado "Object".<br /> Um nó de objeto não pode conter nenhum elemento filho.<br /> Somente nós de reconhecedor personalizados podem conter nós de objeto.<br /> | 
| <span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl><dt><strong>GUID_CNT_PARAGRAPH</strong></dt><dt>(parágrafo)</dt></dl> | Representa um nó para uma coleção de nós que constitui um agrupamento lógico de linhas.<br /> A definição exata de um parágrafo é determinada pelos mecanismos de análise. Em geral, um parágrafo contém grupos de linhas que podem fluir juntos se a caixa que contém as linhas fosse redimensionada.<br /> Um nó de parágrafo pode conter os seguintes tipos de elementos filho:<br /><ul><li>Qualquer número de nós de marcador de tinta.</li><li>Qualquer número de nós de linha.</li><li>Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</li></ul> | 
| <span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl><dt><strong>GUID_CNT_ROOT</strong></dt><dt>(raiz)</dt></dl> | Representa um nó para o nó superior de uma árvore de nós que descreve os resultados da análise de tinta.<br /> Nós raiz geralmente são obtidos do método de <a href="iinkanalyzer-getrootnode.md"><strong>método IInkAnalyzer:: GetRootNode</strong></a> .<br /> Um nó raiz pode conter os seguintes tipos de elementos filho:<br /><ul><li>Qualquer número de nós de dica de análise.</li><li>Qualquer número de nós de reconhecedor personalizados.</li><li>Qualquer número de nós de imagem.</li><li>Qualquer número de nós de desenho de tinta.</li><li>Qualquer número de nós de região de gravação.</li><li>Qualquer número de nós de tinta não classificados.</li><li>Qualquer número de nós com um valor de <strong>GUID</strong> desconhecido.</li></ul> | 
| <span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl><dt><strong>GUID_CNT_TEXTWORD</strong></dt><dt>(textword)</dt></dl> | Representa um nó para a região bidimensional em que qualquer texto que não seja de tinta pode existir no documento.<br /> O <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> não produz os nós da palavra de texto. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para adicionar um nó de texto da palavra à árvore de nós de contexto. Em seguida, o <strong>IInkAnalyzer</strong> usa as regiões definidas pelo nó texto da palavra para determinar se alguma tinta anota o texto não-à tinta.<br /> Os reconhecedores futuros podem usar a região definida por um nó de palavra de texto para determinar se alguma tinta anota a palavra que não é de tinta.<br /> Um nó de palavra de texto não pode ter nenhum elemento filho<br /> | 
| <span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt><dt>(UnclassifiedInk)</dt></dl> | Representa um nó para todos os traços que ainda não foram classificados ou reconhecidos.<br /> Um nó de tinta não classificado não pode ter nenhum elemento filho.<br /> | 




## <a name="remarks"></a>Comentários

Para obter mais informações sobre os diferentes tipos de nó de contexto, consulte [visão geral da análise de tinta](ink-analysis-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




