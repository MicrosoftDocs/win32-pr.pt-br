---
description: inicia Windows ajuda (Winhelp.exe) e passa dados adicionais que indicam a natureza da ajuda solicitada pelo aplicativo.
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

\[essa função está disponível por meio do Windows XP e do Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

inicia Windows ajuda (Winhelp.exe) e passa dados adicionais que indicam a natureza da ajuda solicitada pelo aplicativo.

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

*hWndMain* \[ no\]
</dt> <dd>

Digite: **HWND**

Um identificador para a janela que solicita ajuda. A função **MLWinHelp** usa esse identificador para controlar quais aplicativos solicitaram ajuda. Se o parâmetro *uCommand* especificar Help \_ CONTEXTMENU ou Help \_ WM \_ Help, *hWndMain* identificará o controle que solicita ajuda.

</dd> <dt>

*lpszHelp* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

O endereço de uma cadeia de caracteres terminada em nulo que contém o caminho, se necessário, e o nome do arquivo de ajuda que **MLWinHelp** será exibido.

O nome do arquivo pode ser seguido por um colchete angular (>) e o nome de uma janela secundária se o tópico for ser exibido em uma janela secundária em vez de na janela principal. Você deve definir o nome da janela secundária na \[ \] seção Windows do arquivo de projeto de ajuda (. hpj).

</dd> <dt>

*uCommand* \[ no\]
</dt> <dd>

Tipo: **uint**

O tipo de ajuda solicitado. Para obter uma lista de valores possíveis e como eles afetam o valor a ser colocado no parâmetro *dwData* , consulte a seção comentários.

</dd> <dt>

*dwData* \[ no\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Dados adicionais. O valor usado depende do valor do parâmetro *uCommand* . Para obter uma lista de possíveis valores de *dwData* , consulte a seção comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Retorna um valor diferente de zero em caso de êxito ou zero caso contrário. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa função não está incluída em um arquivo de cabeçalho e deve ser chamada por ordinal 395 para **MLWinHelpA** e 397 para **MLWinHelpW**.

O **MLWinHelp** é essencialmente um wrapper para o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Ele tenta obter o caminho para o arquivo de ajuda correspondente à configuração de idioma da interface do usuário atual antes de chamar **WinHelp**. Se tiver sucesso, ele passará esse caminho. Se falhar, ele passará o caminho apontado por *lpszHelp*.

Essa função falhará se for chamada de qualquer contexto, mas o usuário atual.

Antes de fechar a janela que solicitou ajuda, o aplicativo deve chamar **MLWinHelp** com o parâmetro *UCOMMAND* definido para ajudar a \_ sair. até que todos os aplicativos tenham feito isso, Windows a ajuda não será encerrada. observe que a chamada de Windows ajuda com o \_ comando help QUIT não será necessária se você tiver usado o \_ comando help CONTEXTPOPUP para iniciar Windows ajuda.

A tabela a seguir mostra os valores possíveis para o parâmetro *uCommand* e os formatos correspondentes do parâmetro *dwData* .



| *uCommand*          | Ação                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| comando de ajuda \_       | Executa uma macro de ajuda ou uma cadeia de caracteres de macro.                                                                                                                                                                                                                               | Endereço de uma cadeia de caracteres que especifica o nome da macro (s) de ajuda a ser executada. Se a cadeia de caracteres especificar vários nomes de macro, os nomes deverão ser separados por ponto e vírgula. você deve usar a forma abreviada do nome da macro para algumas macros porque Windows ajuda não oferece suporte ao nome longo.                         |
| conteúdo da ajuda \_      | Exibe o tópico especificado pela opção Contents na \[ seção Options \] do arquivo. hpj. Este comando é para compatibilidade com versões anteriores. Novos aplicativos devem fornecer um arquivo. CNT e usar o \_ comando help Finder.                                           | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
| contexto de ajuda \_       | Exibe o tópico identificado pelo identificador de contexto especificado definido na \[ seção mapa \] do arquivo. hpj.                                                                                                                                                   | Contém o identificador de contexto para o tópico.                                                                                                                                                                                                                                                               |
| CONTEXTMENU da ajuda \_   | Exibe o menu **ajuda** da janela selecionada e, em seguida, exibe o tópico para o controle selecionado em uma janela pop-up.                                                                                                                                             | Endereço de uma matriz de pares **DWORD** . A primeira **DWORD** em cada par é o identificador de controle, e o segundo é o identificador de contexto para o tópico. A matriz deve ser terminada por um par de zeros {0,0} . Se você não quiser adicionar ajuda a um controle específico, defina seu identificador de contexto como-1. |
| CONTEXTPOPUP de ajuda \_  | Exibe o tópico identificado pelo identificador de contexto especificado definido na \[ seção mapa \] do arquivo. hpj em uma janela pop-up.                                                                                                                                | Contém o identificador de contexto para um tópico.                                                                                                                                                                                                                                                                 |
| \_localizador de ajuda        | Exibe a caixa de diálogo **Tópicos da ajuda** .                                                                                                                                                                                                                             | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
| AJUDA do \_ forcefile     | garante que Windows ajuda esteja exibindo o arquivo de ajuda correto. se o arquivo de ajuda incorreto estiver sendo exibido, Windows ajuda abrirá o correto; caso contrário, não há nenhuma ação.                                                                                     | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
| HELPONHELP de ajuda \_    | exibe a ajuda sobre como usar Windows ajuda, se o arquivo Winhlp32. hlp estiver disponível.                                                                                                                                                                                     | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
| índice da ajuda \_         | Exibe o tópico especificado pela opção Contents na \[ seção Options \] do arquivo. hpj. Este comando é para compatibilidade com versões anteriores. Os novos aplicativos devem usar o \_ comando do localizador da ajuda.                                                                   | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
| chave de ajuda \_           | Exibe o tópico na tabela de palavras-chave que corresponde à palavra-chave especificada, se houver uma correspondência exata. Se houver mais de uma correspondência, o exibirá o índice com os tópicos listados na caixa de listagem **Tópicos encontrados** .                                                 | Endereço de uma cadeia de caracteres de palavra-chave. Várias palavras-chave devem ser separadas por ponto e vírgula.                                                                                                                                                                                                                              |
| MULTIKEY de ajuda \_      | Exibe o tópico especificado por uma palavra-chave em uma tabela de palavras-chave alternativa.                                                                                                                                                                                           | Endereço de uma estrutura [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que especifica um caractere de nota de rodapé de tabela e uma palavra-chave.                                                                                                                                                                                     |
| PARTIALKEY de ajuda \_    | Exibe o tópico na tabela de palavras-chave que corresponde à palavra-chave especificada, se houver uma correspondência exata. Se houver mais de uma correspondência, o exibirá a caixa de diálogo **Tópicos encontrados** . Para exibir o índice sem passar uma palavra-chave, use um ponteiro para uma cadeia de caracteres vazia. | Endereço de uma cadeia de caracteres de palavra-chave. Várias palavras-chave devem ser separadas por ponto e vírgula.                                                                                                                                                                                                                              |
| AJUDA para \_ sair          | informa Windows ajuda de que ele não é mais necessário. se nenhum outro aplicativo tiver solicitado ajuda, Windows fechará Windows ajuda.                                                                                                                                         | Aceita Defina como 0.                                                                                                                                                                                                                                                                                           |
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
| Cabeçalho<br/>                   | <dl> <dt>Nenhum</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **MLWinHelpW** (Unicode) e **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
