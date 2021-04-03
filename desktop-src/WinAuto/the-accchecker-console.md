---
title: O console do AccChecker
description: AccChecker console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do seu aplicativo.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Console do AccChecker
- Ferramenta de linha de comando AccChecker
- linha de comando, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822338"
---
# <a name="the-accchecker-console"></a>O console do AccChecker

AccChecker console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do seu aplicativo. A linha de comando aceita uma variedade de entradas (como HWND, título da janela e rotina de verificação) e fornece um código de saída que corresponde à contagem de log de erros.

-   [Sintaxe de linha de comando](#command-line-syntax)
-   [Códigos de erro de linha de comando](#command-line-error-codes)
-   [Exemplos de linha de comando](#command-line-examples)
-   [Tópicos relacionados](#related-topics)

![ferramenta de linha de comando do console do accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

O console do AccChecker tem a seguinte sintaxe de linha de comando.

**Opções de AccCheckConsole \[ \] (-HWND <hwnd> \| -process <name> ) \[<dlls>\]**

As opções de linha de comando são as seguintes.



| Opções                                                                                                                                                         | Descrição                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd><br/>                                                                     | Valida a janela que tem o identificador especificado (HWND). O identificador pode ser especificado em hexadecimal ou Decimal.<br/> |
| <span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-janela <title><br/>                                                            | Valida a janela que tem o título especificado.<br/>                                                                |
| <span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processo <name><br/>                       | Valida a janela principal do processo que tem o nome especificado.<br/>                                             |
| <span id="____________________________-list"></span><span id="____________________________-LIST"></span> -lista<br/>                                       | Lista todas as rotinas de verificação disponíveis.<br/>                                                                 |
| <span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -habilitar <name><br/>                          | Executa a rotina de verificação especificada. Essa opção pode ser especificada mais de uma vez.<br/>                             |
| <span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -desabilitar <name><br/> | Executa tudo, exceto a rotina de verificação especificada. Essa opção pode ser especificada mais de uma vez.<br/>                     |
| <span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (erro de aviso de informação \| \| )<br/>                          | A classificação de eventos mais baixa que será registrada em log.<br/>                                                                      |
| <span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -Logfile <file><br/>                       | Grave a saída no arquivo de log especificado. Essa opção pode ser especificada mais de uma vez.<br/>                          |
| <span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suprimir <file><br/>                                                         | Use o arquivo XML especificado para suprimir erros. <br/>                                                                   |
| <span id="-quiet"></span><span id="-QUIET"></span>-Quiet<br/>                                                                                             | Não grave a saída de log para stdout.<br/>                                                                            |
| <span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-ajuda <br/>                           | Exibe a ajuda rápida. <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a>Códigos de erro de linha de comando

Veja a seguir os códigos de erro retornados de AccCheckConsole ao usar "Echo% ERRORLEVEL%"



| Código do erro                       | Descrição                                 |
|----------------------------------|---------------------------------------------|
| <span id="0"></span>0<br/> | Nenhum erro e nenhum aviso.<br/>       |
| <span id="1"></span>1<br/> | Instrução Usages foi solicitada. <br/> |
| <span id="2"></span>2<br/> | Erros e nenhum aviso.<br/>          |
| <span id="3"></span>Beta<br/> | Erros e avisos.<br/>             |
| <span id="4"></span>4<br/> | Avisos, mas sem erros.<br/>          |
| <span id="5"></span>05<br/> | Linha de comando inválida. <br/>           |



 

## <a name="command-line-examples"></a>Exemplos de linha de comando

A seguir estão vários exemplos de linha de comando do console AccChecker.

-   Executar todas as verificações em uma janela com um nome especificado.

    **AccCheckConsole-janela "sem título – bloco de notas"**

-   Executar um subconjunto das verificações em um HWND, especificando um arquivo de supressão.

    **AccCheckConsole-HWND 0x00382f00-habilitar CheckTabbing-habilitar CHECKNAME-suprime suppress.xml**

-   Execute todas as verificações de uma nova DLL de verificação.

    **AccCheckConsole-janela "sem título-bloco de notas" VerificationRoutine1.dll**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





