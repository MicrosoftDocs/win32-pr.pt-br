---
description: Inicia Windows ajuda (Winhelp.exe) e passa dados adicionais que indicam a natureza da ajuda solicitada pelo aplicativo.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: Função MLWinHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: a6c109f39107ba3cfd1800cca8db516d0033a2f3c32b9784e4359b3c6c50655d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968895"
---
# <a name="mlwinhelp-function"></a>Função MLWinHelp

\[Essa função está disponível por meio Windows XP e Windows Server 2003. Ele pode ser alterado ou não disponível nas versões subsequentes do Windows.\]

Inicia Windows ajuda (Winhelp.exe) e passa dados adicionais que indicam a natureza da ajuda solicitada pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWndMain* \[ Em\]
</dt> <dd>

Digite: **HWND**

Um alça para a janela solicitando ajuda. A **função MLWinHelp** usa esse controle para controlar quais aplicativos solicitaram ajuda. Se o *parâmetro uCommand* especificar HELP \_ CONTEXTMENU ou HELP WM \_ \_ HELP, *hWndMain identificará* o controle solicitando ajuda.

</dd> <dt>

*lpszHelp* \[ Em\]
</dt> <dd>

Tipo: **LPCTSTR**

O endereço de uma cadeia de caracteres terminada em nulo que contém o caminho, se necessário, e o nome do arquivo de ajuda que **MLWinHelp** deve exibir.

O nome do arquivo pode ser seguido por um colchete angular (>) e o nome de uma janela secundária se o tópico deve ser exibido em uma janela secundária em vez de na janela primária. Você deve definir o nome da janela secundária na seção WINDOWS do arquivo do projeto \[ \] de ajuda (.hpj).

</dd> <dt>

*uCommand* \[ Em\]
</dt> <dd>

Tipo: **UINT**

O tipo de ajuda solicitada. Para ver uma lista de valores possíveis e como eles afetam o valor a ser colocado no parâmetro *dwData,* consulte a seção Comentários.

</dd> <dt>

*dwData* \[ Em\]
</dt> <dd>

Tipo: **\_ PTR DWORD**

Dados adicionais. O valor usado depende do valor do *parâmetro uCommand.* Para ver uma lista dos possíveis *valores dwData,* consulte a seção Comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **BOOL**

Retorna um valor diferente de zero em caso de êxito ou zero caso contrário. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa função não está incluída em um arquivo de header e deve ser chamada pelo ordinal 395 para **MLWinHelpA** e 397 para **MLWinHelpW.**

**MLWinHelp** é essencialmente um wrapper para [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Ele tenta obter o caminho para o arquivo de ajuda correspondente à configuração de linguagem de interface do usuário atual antes de chamar **WinHelp**. Se for bem-sucedido, ele passará por esse caminho. Se falhar, ele passará o caminho apontado por *lpszHelp.*

Essa função falhará se for chamada de qualquer contexto, mas do usuário atual.

Antes de fechar a janela que solicitou ajuda, o aplicativo deve chamar **MLWinHelp** com o *parâmetro uCommand* definido como HELP \_ QUIT. Até que todos os aplicativos tenham feito isso, Windows Ajuda não será encerrada. Observe que chamar Windows ajuda com o comando HELP QUIT não será necessário se você tiver usado o \_ comando HELP CONTEXTPOPUP para iniciar \_ Windows Ajuda.

A tabela a seguir mostra os valores possíveis para o *parâmetro uCommand* e os formatos correspondentes do *parâmetro dwData.*



| *uCommand*          | Ação                                                                                                                                                                                                                                                               | *Dwdata*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMANDO \_ HELP       | Executa uma macro de ajuda ou uma cadeia de caracteres de macro.                                                                                                                                                                                                                               | Endereço de uma cadeia de caracteres que especifica o nome das macros de ajuda a executar. Se a cadeia de caracteres especificar vários nomes de macro, os nomes deverão ser separados por ponto e vírgula. Você deve usar a forma curta do nome da macro para algumas macros porque Windows Ajuda não dá suporte ao nome longo.                         |
| CONTEÚDO DA \_ AJUDA      | Exibe o tópico especificado pela opção Conteúdo na seção \[ OPÇÕES \] do arquivo .hpj. Esse comando é para compatibilidade com compatibilidade com 244 Novos aplicativos devem fornecer um arquivo .cnt e usar o comando HELP \_ FINDER.                                           | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| CONTEXTO \_ DA AJUDA       | Exibe o tópico identificado pelo identificador de contexto especificado definido na \[ seção MAP do arquivo \] .hpj.                                                                                                                                                   | Contém o identificador de contexto para o tópico.                                                                                                                                                                                                                                                               |
| HELP \_ CONTEXTMENU   | Exibe o menu **Ajuda** para a janela selecionada e, em seguida, exibe o tópico para o controle selecionado em uma janela pop-up.                                                                                                                                             | Endereço de uma matriz de **pares DWORD.** A primeira **DWORD** em cada par é o identificador de controle e a segunda é o identificador de contexto para o tópico. A matriz deve ser encerrada por um par de {0,0} zeros. Se você não quiser adicionar ajuda a um controle específico, de definido seu identificador de contexto como -1. |
| HELP \_ CONTEXTPOPUP  | Exibe o tópico identificado pelo identificador de contexto especificado definido na seção MAP do \[ \] arquivo .hpj em uma janela pop-up.                                                                                                                                | Contém o identificador de contexto para um tópico.                                                                                                                                                                                                                                                                 |
| HELP \_ FINDER        | Exibe a caixa **de diálogo Tópicos da** Ajuda.                                                                                                                                                                                                                             | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ FORCEFILE     | Garante que Windows Ajuda está exibindo o arquivo de ajuda correto. Se o arquivo de ajuda incorreto estiver sendo exibido, Windows Ajuda abrirá o correto; caso contrário, não haverá nenhuma ação.                                                                                     | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ HELPONHELP    | Exibe ajuda sobre como usar a Windows, se o arquivo Winhlp32.hlp estiver disponível.                                                                                                                                                                                     | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| ÍNDICE \_ DE AJUDA         | Exibe o tópico especificado pela opção Conteúdo na seção \[ OPÇÕES \] do arquivo .hpj. Esse comando é para compatibilidade com compatibilidade com 244 Novos aplicativos devem usar o comando HELP \_ FINDER.                                                                   | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| CHAVE DE \_ AJUDA           | Exibe o tópico na tabela de palavras-chave que corresponde à palavra-chave especificada, se houver uma combinação exata. Se houver mais de uma combinação, o exibirá o índice com os tópicos listados na **caixa de listagem Tópicos** Encontrados.                                                 | Endereço de uma cadeia de caracteres de palavra-chave. Várias palavras-chave devem ser separadas por ponto e vírgula.                                                                                                                                                                                                                              |
| AJUDA \_ MULTIKEY      | Exibe o tópico especificado por uma palavra-chave em uma tabela de palavras-chave alternativa.                                                                                                                                                                                           | Endereço de uma [**estrutura MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que especifica um caractere de nota de rodapé de tabela e uma palavra-chave.                                                                                                                                                                                     |
| AJUDA \_ PARTIALKEY    | Exibe o tópico na tabela de palavras-chave que corresponde à palavra-chave especificada, se houver uma combinação exata. Se houver mais de uma combinação, exibirá a caixa **de diálogo Tópicos** Encontrados. Para exibir o índice sem passar uma palavra-chave, use um ponteiro para uma cadeia de caracteres vazia. | Endereço de uma cadeia de caracteres de palavra-chave. Várias palavras-chave devem ser separadas por ponto e vírgula.                                                                                                                                                                                                                              |
| AJUDA \_ PARA SAIR          | Informa Windows Ajuda de que ela não é mais necessária. Se nenhum outro aplicativo tiver solicitado ajuda, Windows fechará Windows Ajuda.                                                                                                                                         | Ignorado; definido como 0.                                                                                                                                                                                                                                                                                           |
| conconteúdos da ajuda \_   | Especifica o tópico de conteúdo. Windows A ajuda exibirá este tópico quando o usuário clicar no botão **conteúdo** se o arquivo de ajuda não tiver um arquivo. CNT associado.                                                                                                  | Contém o identificador de contexto para o tópico de conteúdo.                                                                                                                                                                                                                                                      |
| REO pos do HELP \_ SETpopup \_ | Define a posição da janela pop-up subsequente.                                                                                                                                                                                                                   | Contém os dados da posição. Use a macro [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) para concatenar as coordenadas horizontal e vertical em um único valor. A janela pop-up é posicionada como se o cursor do mouse estivesse no ponto especificado quando a janela pop-up fosse chamada.                                 |
| SETWINPOS de ajuda \_     | exibe a janela ajuda do Windows, se ela for minimizada ou na memória, e define seu tamanho e posição conforme especificado.                                                                                                                                                      | Endereço de uma estrutura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) que especifica o tamanho e a posição de uma janela de ajuda primária ou secundária.                                                                                                                                                             |
| TCARD de ajuda \_         | indica que um comando é para uma instância de cartão de treinamento de Windows ajuda. Combine esse comando com outros comandos usando o operador OR                                                                                                                    | Depende do comando com o qual esse comando é combinado.                                                                                                                                                                                                                                                  |
| ajuda do \_ WM Help \_      | Exibe o tópico para o controle identificado pelo parâmetro *hWndMain* em uma janela pop-up.                                                                                                                                                                        | Endereço de uma matriz de pares **DWORD** . A primeira **DWORD** em cada par é um identificador de controle, e o segundo é um identificador de contexto para um tópico. A matriz deve ser terminada por um par de zeros {0,0} . Se você não quiser adicionar ajuda a um controle específico, defina seu identificador de contexto como-1.       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Nenhuma</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **MLWinHelpW** (Unicode) e **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
