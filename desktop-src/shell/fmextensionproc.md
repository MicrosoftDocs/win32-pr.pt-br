---
description: Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.
title: Função de retorno de chamada FMExtensionProc (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842237"
---
# <a name="fmextensionproc-callback-function"></a>Função de retorno de chamada FMExtensionProc

Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.

## <a name="syntax"></a>Sintaxe


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Digite: **HWND**

Um identificador de janela para o Gerenciador de arquivos. Uma extensão usa esse identificador para especificar a janela pai de qualquer caixa de diálogo ou caixa de mensagem que deve ser exibida e para enviar mensagens de consulta ao Gerenciador de arquivos.

</dd> <dt>

*wMsg* 
</dt> <dd>

Tipo: **Word**

Uma das mensagens do Gerenciador de arquivos a seguir.

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 a 99**


</dt> <dd>

O usuário selecionou um item no menu fornecido pela extensão. O valor é o identificador do item de menu selecionado.

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

O usuário pressionou F1 ao selecionar um menu de extensão ou um item de comando de barra de ferramentas. Indica que a extensão deve chamar **WinHelp** adequadamente para o item de comando.

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HelpString**


</dt> <dd>

O usuário selecionou um menu de extensão ou um item de comando de barra de ferramentas. Indica que a extensão deve fornecer uma cadeia de caracteres de ajuda.

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

O usuário selecionou o menu da extensão. A extensão deve inicializar itens no menu.

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**


</dt> <dd>

O Gerenciador de Arquivos está carregando a DLL de extensão e solicita à DLL informações sobre o menu que a DLL fornece.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

A seleção na janela **de diretório do Gerenciador** de Arquivos ou na janela Resultados **da** Pesquisa foi alterada.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**BARRA DE FERRAMENTAS \_ FMEVENTLOAD**


</dt> <dd>

O Gerenciador de Arquivos está criando a barra de ferramentas e solicita à DLL de extensão informações sobre os botões que a DLL adiciona à barra de ferramentas.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**


</dt> <dd>

O Gerenciador de Arquivos está descarregando a DLL de extensão.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ATUALIZAÇÃO DO USUÁRIO \_ \_ FMEVENT**


</dt> <dd>

O usuário **selecionou o** comando Atualizar no menu **Janela.** A extensão deve atualizar itens no menu, se necessário.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **LONG**

Valor específico da mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LONG**

Retorna um valor dependente da mensagem *de parâmetro wMsg.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




