---
title: O Console do AccChecker
description: O AccChecker Console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do aplicativo.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- AccChecker Console
- Ferramenta de linha de comando AccChecker
- linha de comando, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272447e2513f109206af6fedaaf6adffe665e8b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887039"
---
# <a name="the-accchecker-console"></a>O Console do AccChecker

O AccChecker Console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do aplicativo. A linha de comando aceita uma variedade de entradas (como HWND, título da janela e rotina de verificação) e fornece um código de saída que corresponde à contagem de log de erros.

-   [Sintaxe de linha de comando](#command-line-syntax)
-   [Códigos de erro de linha de comando](#command-line-error-codes)
-   [Exemplos de linha de comando](#command-line-examples)
-   [Tópicos relacionados](#related-topics)

![ferramenta de linha de comando do console do accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

O Console do AccChecker tem a seguinte sintaxe de linha de comando.

**Opções de AccCheckConsole \[ \] (-hwnd &lt; hwnd &gt; \| -process &lt; name ) &gt; \[ &lt; dlls&gt;\]**

As opções de linha de comando são as a seguir.



| Opções                                                                                                                                                         | Descrição                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd &lt; hwnd&gt;<br/>                                                                     | Valida a janela que tem o HWND (handle especificado). O handle pode ser especificado em hexidecimal ou decimal.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window &lt; title&gt;<br/>                                                            | Valida a janela que tem o título especificado.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process &lt; name&gt;<br/>                       | Valida a janela principal do processo que tem o nome especificado.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list<br/>                                       | Lista todas as rotinas de verificação disponíveis.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable &lt; name&gt;<br/>                          | Executa a rotina de verificação especificada. Essa opção pode ser especificada mais de uma vez.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable &lt; name&gt;<br/> | Executa tudo, menos a rotina de verificação especificada. Essa opção pode ser especificada mais de uma vez.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (aviso \| de \| informações err)<br/>                          | A classificação de evento mais baixa que será registrada.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile &lt; file&gt;<br/>                       | Gravar a saída no arquivo de log especificado. Essa opção pode ser especificada mais de uma vez.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress &lt; file&gt;<br/>                                                         | Use o arquivo XML especificado para suprimir erros. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-quiet<br/>                                                                                             | Não gravar saída de log em stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help <br/>                           | Exibe ajuda rápida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Códigos de erro de linha de comando

A seguir estão os códigos de erro retornados de AccCheckConsole ao usar "echo %errorlevel%"



| Código do erro                       | Descrição                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Nenhum erro e nenhum aviso.<br/>       |
| <span id="1"></span>1<br/> | A instrução Usages foi solicitada. <br/> |
| <span id="2"></span>2<br/> | Erros e nenhum aviso.<br/>          |
| <span id="3"></span>3<br/> | Erros e avisos.<br/>             |
| <span id="4"></span>4<br/> | Avisos, mas nenhum erro.<br/>          |
| <span id="5"></span>5<br/> | Linha de comando inválida. <br/>           |



 

## <a name="command-line-examples"></a>Exemplos de linha de comando

A seguir estão vários exemplos de linha de comando do Console do AccChecker.

-   Execute todas as verificações em uma janela com um nome especificado.

    **AccCheckConsole -window "Sem título - Bloco de notas"**

-   Execute um subconjunto das verificações em um HWND, especificando um arquivo de supressão.

    **AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**

-   Execute todas as verificações de uma nova DLL de verificação.

    **AccCheckConsole -window "Untitled - Bloco de notas" VerificationRoutine1.dll**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





