---
title: Estilos estendidos do controle ComboBoxEx (CommCtrl.h)
description: Dar suporte aos estilos estendidos listados nesta seção, bem como à maioria dos estilos de controle de caixa de combinação padrão.
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
ms.openlocfilehash: aed3ca32fa063b9b824a2ecd444a6a71c1885697f839b67e117c75622f009c60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921146"
---
# <a name="comboboxex-control-extended-styles"></a>Estilos estendidos do controle ComboBoxEx

Dar suporte aos estilos estendidos listados nesta seção, bem como à maioria dos estilos de controle de caixa de combinação padrão.



| Constante                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ EX \_ CASESENSITIVE**</dt> </dl>             | **As pesquisas BSTR** na lista serão sensíveis a minúsculas. Isso inclui pesquisas como resultado do texto que está sendo digitado na caixa de edição e da mensagem CB \_ FINDSTRINGEXACT.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | A caixa de edição e a lista suspenso não exibirão imagens de item. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | A caixa de edição e a lista suspenso não exibirão imagens de item. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | Permite que o controle ComboBoxEx seja dimensionado verticalmente menor do que seu controle de caixa de combinação contido. Se o ComboBoxEx for dimensionado menor que a caixa de combinação, a caixa de combinação será recortada. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | Windows NT apenas. A caixa de edição usará os caracteres de barra (/), barra invertida ( ) e \\ ponto (.) como delimitadores de palavras. Isso torna os atalhos de teclado para a movimentação de cursor palavra a palavra efetiva em nomes de caminho e URLs.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista e posterior.** Faz com que os itens na lista de listas e na caixa de edição (quando a caixa de edição é somente leitura) sejam truncados com reellipses ("...") em vez de apenas recortados pela borda do controle. Isso é útil quando o controle precisa ser definido com uma largura fixa, mas as entradas na lista podem ser longas.<br/> |



## <a name="remarks"></a>Comentários

Defina e recupere os estilos estendidos da caixa de combinação usando as mensagens [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) e [**CBEM \_ GETEXTENDEDSTYLE.**](cbem-getextendedstyle.md)

> [!Note]  
> Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o estilo [**CBS \_ SIMPLE,**](combo-box-styles.md) ele poderá não ser reintint corretamente. O **estilo CBS \_ SIMPLE** também não funciona corretamente com o estilo estendido CBES \_ EX \_ PATHWORDBREAKPROC.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





