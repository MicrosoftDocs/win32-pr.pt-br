---
description: Exibe uma janela de ajuda que corresponde à configuração de idioma da interface do usuário atual.
title: Função MLHtmlHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: 38d331d57b9484ab6d7a505d929508f30d510ad8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841207"
---
# <a name="mlhtmlhelp-function"></a>Função MLHtmlHelp

\[Essa função está disponível por meio do Windows XP e do Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Exibe uma janela de ajuda que corresponde à configuração de idioma da interface do usuário atual.

## <a name="syntax"></a>Sintaxe


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndCaller* \[ no\]
</dt> <dd>

Digite: **HWND**

Um identificador para a janela pai que chama essa função.

</dd> <dt>

*pszFile* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para um buffer que contém o caminho totalmente qualificado de um arquivo de ajuda compilado (. chm) ou um arquivo de tópico dentro de um arquivo de ajuda especificado.

</dd> <dt>

*uCommand* \[ no\]
</dt> <dd>

Tipo: **uint**

O comando a ser concluído. Essa função dá suporte diretamente somente ao [ \_ \_ tópico de exibição hh](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) e ao [ \_ \_ \_ pop-up exibir texto](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). No caso de qualquer outro comando, a chamada é encaminhada sem o valor de *dwCrossCodePage* para [HTMLHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ no\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Todos os dados que podem ser necessários, com base no valor do parâmetro *uCommand* .

</dd> <dt>

*dwCrossCodePage* \[ no\]
</dt> <dd>

Tipo: **DWORD**

O **valor DWORD** que indica a página de código da configuração de linguagem de interface do usuário atual, como CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Digite: **HWND**

Dependendo do *uCommand* especificado e do resultado, **MLHtmlHelp** retorna um ou ambos os seguintes:

-   O handle (hwnd) da janela de ajuda.
-   **NULL**. Em alguns casos, **NULL** indica falha; em outros casos, **NULL** indica que a janela de ajuda ainda não foi criada.

## <a name="remarks"></a>Comentários

Se surgir um problema com o caminho do arquivo de ajuda para a linguagem atual, a chamada será encaminhada para [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para manipulação padrão.

Quando a janela de ajuda é fechada, o foco retorna para o proprietário, a menos que o proprietário seja a área de trabalho. Se *hwndCaller for* a área de trabalho, o sistema operacional determinará onde o foco será retornado.

Além disso, se **MLHtmlHelp** enviar qualquer mensagem de notificação da janela de ajuda, as [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) mensagens serão enviadas para *hwndCaller,* desde que você tenha habilitado o acompanhamento de mensagens de notificação na definição da janela de ajuda.

## <a name="examples"></a>Exemplos

O exemplo a seguir chama o comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir o arquivo de ajuda chamado Help.chm e exibir seu tópico padrão na janela de ajuda chamada `Mainwin` . Em geral, a janela de ajuda especificada neste comando é um [Visualizador da Ajuda HTML padrão.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Ao usar essa função, de definido o tamanho da pilha do executável de hospedagem como pelo menos 100 mil. Se o tamanho da pilha definido for muito pequeno, o thread criado para executar a Ajuda HTML também será criado com esse tamanho de pilha e a operação poderá falhar. Opcionalmente, você pode remover /STACK da linha de comando do link e também remover qualquer configuração stack no arquivo DEF do executável (nesse caso, o tamanho padrão da pilha é de 1 MB). Você também pode definir o tamanho da pilha usando o comando do compilador /Fnumber (o compilador passará isso para o linker como /STACK).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2003 \[\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Nenhum</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5.0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **MLHtmlHelpW** (Unicode) e **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
