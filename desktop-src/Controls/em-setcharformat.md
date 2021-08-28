---
title: Mensagem de EM_SETCHARFORMAT (RichEdit. h)
description: Define a formatação de caracteres em um controle de edição rico.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- controles de Windows de mensagem de EM_SETCHARFORMAT
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100cfb1d322cde2d411a0298ee86c224899669defc585826b16bf96751bb4639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673126"
---
# <a name="em_setcharformat-message"></a>\_Mensagem em SETCHARFORMAT

Define a formatação de caracteres em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Formatação de caractere que se aplica ao controle. Se esse parâmetro for zero, o formato de caractere padrão será definido. Caso contrário, pode ser um dos valores a seguir.



| Valor                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ todos**</dt> </dl>                                     | Aplica a formatação a todo o texto no controle. Não é válido **com \_ seleção de SCF** ou **\_ palavra SCF**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4,1:** Associa uma fonte a um determinado script, alterando assim a fonte padrão para esse script. Para especificar a fonte, use os seguintes membros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4,1:** Associa uma fonte substituta (plano-2) a um determinado script, alterando assim a fonte padrão para esse script. Para especificar a fonte, use os seguintes membros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | Obtém o caractere repertório do LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**padrão de SCF \_**</dt> </dl>                         | **RichEdit 4,1:** Define a fonte padrão do controle. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**\_DONTSETDEFAULT SPF**</dt> </dl>    | Impede a definição do formato de parágrafo padrão quando o controle rich edit está vazio.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4,1:** Impede a alternância de teclado para corresponder à fonte. Por exemplo, se uma fonte em árabe for definida, normalmente o recurso de teclado automático para idiomas bidi altera o teclado para um teclado árabe.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**seleção de SCF \_**</dt> </dl>                   | Aplica a formatação à seleção atual. Se a seleção estiver vazia, a formatação de caractere será aplicada ao ponto de inserção e o novo formato de caractere estará em vigor somente até que o ponto de inserção seja alterado.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF \_ SETpadrão**</dt> </dl>                | Define os atributos de formatação de parágrafo padrão.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | Aplique a fonte somente se ela puder manipular o script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4,1:** Usado com **a \_ seleção de SCF**. Indica que o formato veio de uma barra de ferramentas ou outra ferramenta de interface do usuário, para que as regras de formatação da interface do usuário sejam usadas em vez da formatação literal.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**palavra do SCF \_**</dt> </dl>                                  | Aplica a formatação à palavra ou às palavras selecionadas. Se a seleção estiver vazia, mas o ponto de inserção estiver dentro de uma palavra, a formatação será aplicada à palavra. O valor da **\_ palavra SCF** deve ser usado em conjunto com o valor de **\_ seleção de SCF** .<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) especificando a formatação de caractere a ser usada. Somente os atributos de formatação especificados pelo membro **dwMask** são alterados.

Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que é uma extensão da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) . Antes de enviar a mensagem em **\_ SETCHARFORMAT** , defina o membro **cbSize** da estrutura como `sizeof(CHARFORMAT)` ou `sizeof(CHARFORMAT2)` indique qual versão da estrutura está sendo usada.

Os membros **szFaceName** e **bCharSet** podem ser sobreréguas quando forem inválidos para caracteres, por exemplo: Arial em caracteres kanji.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Se essa mensagem for enviada mais de uma vez com os mesmos parâmetros, o efeito no texto será alternado. Ou seja, enviar a mensagem uma vez produz o efeito, enviar a mensagem duas vezes cancela o efeito e assim por diante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





