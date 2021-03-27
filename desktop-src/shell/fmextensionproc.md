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
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988735"
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

Tipo: **HWND**

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

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ carga**


</dt> <dd>

O Gerenciador de arquivos está carregando a DLL de extensão e solicita ao DLL informações sobre o menu que a DLL fornece.

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

A seleção na janela de diretório do **Gerenciador de arquivos** ou na janela **resultados da pesquisa** foi alterada.

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

O Gerenciador de arquivos está criando a barra de ferramentas e solicita a DLL de extensão para obter informações sobre os botões que a DLL adiciona à barra de ferramentas.

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**descarregamento de FMEVENT \_**


</dt> <dd>

O Gerenciador de arquivos está descarregando a DLL de extensão.

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_atualização do usuário do FMEVENT \_**


</dt> <dd>

O usuário selecionou o comando **Atualizar** no menu **janela** . A extensão deve atualizar itens no menu, se necessário.

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

Tipo: **longo**

Valor específico da mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **longo**

Retorna um valor dependente da mensagem de parâmetro *wMsg* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **FMExtensionProcW** (Unicode)<br/>                                          |



 

 




