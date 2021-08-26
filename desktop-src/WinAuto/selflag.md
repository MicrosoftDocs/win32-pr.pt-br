---
title: Constantes SELFLAG (OleAcc. h)
description: Este tópico descreve os valores constantes usados para especificar como um objeto acessível é selecionado ou leva em foco.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b4d0384b66919a55d55593d2e16c9a187d84ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478572"
---
# <a name="selflag-constants"></a>Constantes SELFLAG

Este tópico descreve os valores constantes usados para especificar como um objeto acessível é selecionado ou leva em foco. As constantes são definidas em OleAcc. h e são usadas com o método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .

As seguintes combinações não são permitidas:

-   SELFLAG \_ ADDselecting \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDselecting \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Observação para clientes:** O Microsoft Acessibilidade Ativa não oferece suporte à seleção do texto contido em controles editar e Rich Edit porque o texto é exposto como uma cadeia de caracteres na [propriedade Value](value-property.md)do objeto.

Para obter informações sobre como executar operações de seleção complexas, consulte [selecionando objetos filho](selecting-child-objects.md).




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl><dt><strong>SELFLAG_NONE</strong></dt><dt>0</dt></dl> | Não executa nenhuma ação. O Microsoft Acessibilidade Ativa não altera a seleção ou o foco.<br /> | 
| <span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl><dt><strong>SELFLAG_TAKEFOCUS</strong></dt><dt>0x1</dt></dl> | Define o foco para o objeto e o transforma na âncora de seleção. Usado por si só, esse sinalizador não altera a seleção. o efeito é semelhante a mover o foco manualmente pressionando uma tecla de seta enquanto mantém pressionada a tecla CTRL no Windows Explorer ou em qualquer caixa de listagem de seleção múltipla. <br /> Com objetos que têm o <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS é combinado com os seguintes valores:<br /><ul><li>SELFLAG_TAKESELECTION</li><li>SELFLAG_EXTENDSELECTION</li><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li><li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li></ul>Se você chamar <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> com o sinalizador SELFLAG_TAKEFOCUS em um objeto que tem um <strong>HWND</strong>, o sinalizador entrará em vigor somente se o pai do objeto já tiver o foco.<br /> | 
| <span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl><dt><strong>SELFLAG_TAKESELECTION</strong></dt><dt>0x2</dt></dl> | Seleciona o objeto e remove a seleção de todos os outros objetos no contêiner. <br /> A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção. O SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a clicar uma vez em um item no Windows Explorer.<br /> Esse sinalizador não deve ser combinado com os seguintes sinalizadores:<br /><ul><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_EXTENDSELECTION</li></ul> | 
| <span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt><dt>0x4</dt></dl> | Altera a seleção de forma que todos os objetos entre a âncora de seleção e esse objeto tenham o estado de seleção do objeto de âncora. Se o objeto de âncora não for selecionado, os objetos serão removidos da seleção. Se o objeto Anchor for selecionado, a seleção será estendida para incluir esse objeto e todos os objetos entre eles. Defina o estado de seleção combinando esse sinalizador com SELFLAG_ADDSELECTION ou SELFLAG_REMOVESELECTION. <br /> A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção. O SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a adicionar um item a uma seleção manualmente, mantendo a tecla SHIFT pressionada e clicando em um objeto não selecionado no Windows Explorer.<br /> Esse sinalizador não é combinado com SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl><dt><strong>SELFLAG_ADDSELECTION</strong></dt><dt>0x8</dt></dl> | Adiciona o objeto à seleção atual; o resultado possível é uma seleção não contígua. <br /> A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção. O SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a adicionar um item a uma seleção manualmente, mantendo a tecla CTRL pressionada e clicando em um objeto não selecionado no Windows Explorer.<br /> Esse sinalizador não é combinado com SELFLAG_REMOVESELECTION ou SELFLAG_TAKESELECTION.<br /> | 
| <span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl><dt><strong>SELFLAG_REMOVESELECTION</strong></dt><dt>0x10</dt></dl> | Remove o objeto da seleção atual; o resultado possível é uma seleção não contígua. <br /> A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção. O SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a remover um item de uma seleção manualmente, mantendo a tecla CTRL pressionada enquanto clica em um objeto selecionado no Windows Explorer.<br /> Esse sinalizador não é combinado com SELFLAG_ADDSELECTION ou SELFLAG_TAKESELECTION.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>OleAcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Selecionando objetos filho](selecting-child-objects.md)
</dt> </dl>

 

 





