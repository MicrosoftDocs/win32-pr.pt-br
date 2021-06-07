---
title: Estilos estendidos de controle ComboBoxEx (CommCtrl. h)
description: Dê suporte aos estilos estendidos listados nesta seção, bem como a maioria dos estilos de controle de caixa de combinação padrão.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387652"
---
# <a name="comboboxex-control-extended-styles"></a>Estilos estendidos do controle ComboBoxEx

Dê suporte aos estilos estendidos listados nesta seção, bem como a maioria dos estilos de controle de caixa de combinação padrão.



| Constante                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ ex \_ CASESENSITIVE**</dt> </dl>             | As pesquisas **BSTR** na lista serão diferenciadas entre maiúsculas e minúsculas. Isso inclui pesquisas como resultado de texto que está sendo digitado na caixa de edição e na \_ mensagem CB FINDSTRINGEXACT.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGE**</dt> </dl>                   | A caixa de edição e a lista suspensa não exibirão imagens de item. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt> </dl> | A caixa de edição e a lista suspensa não exibirão imagens de item. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ ex \_ NOSIZELIMIT**</dt> </dl>                   | Permite que o controle ComboBoxEx seja verticalmente dimensionado menor do que seu controle de caixa de combinação contido. Se o ComboBoxEx for menor que a caixa de combinação, a caixa de combinação será recortada. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt> </dl> | Somente Windows NT. A caixa de edição usará os caracteres de barra (/), barra invertida ( \\ ) e ponto (.) como delimitadores de palavras. Isso torna os atalhos de teclado para o movimento de cursor de palavra por palavra efetivo em nomes de caminho e URLs.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista e posterior.** Faz com que os itens na lista suspensa e na caixa de edição (quando a caixa de edição é somente leitura) sejam truncados com reticências ("...") em vez de apenas recortados pela borda do controle. Isso é útil quando o controle precisa ser definido com uma largura fixa, mas as entradas na lista podem ser longas.<br/> |



## <a name="remarks"></a>Comentários

Você define e recupera os estilos estendidos da ComboBox usando as mensagens [**CBEM \_ Extended**](cbem-setextendedstyle.md) e [**CBEM \_ getextendedattribute**](cbem-getextendedstyle.md) .

> [!Note]  
> Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o [**estilo \_ simples do CBS**](combo-box-styles.md) , ele poderá não ser redesenhado corretamente. O **estilo \_ simples do CBS** também não funciona corretamente com o \_ \_ estilo estendido CBES ex PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





