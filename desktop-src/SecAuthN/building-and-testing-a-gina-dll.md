---
description: Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de título Winwlx.h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Como criar e testar uma DLL DE LTD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31df8597ca9ad78b8c94efb5610e3c899f7834cb14c9112b15a410c72705a0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883526"
---
# <a name="building-and-testing-a-gina-dll"></a>Como criar e testar uma DLL DE LTD

Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de título Winwlx.h.

> [!Note]  
> As DLLs DE VALOR são ignoradas no Windows Vista.

 

Para testar uma DLL [*DOEI,*](/windows/desktop/SecGloss/g-gly) use o Winlogon.exe de uma versão verificada do sistema operacional, que está disponível com o DDK (Kit de Desenvolvimento de Driver) do Microsoft Windows. A versão verificada do [*Winlogon dá*](/windows/desktop/SecGloss/w-gly) suporte à depuração deGUEAs da seguinte forma:

-   Você pode usar a sintaxe a seguir para criar uma seção no Win.ini para especificar opções de depuração do Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Se especificado, **o LogFile** deve conter o nome totalmente qualificado do arquivo que será usado para registrar informações de depuração. Se o arquivo não existir, ele será criado.

    As **opções DebugFlags** especificam quais tipos de informações de depuração gravar no arquivo de log ou no depurador. **DebugFlags** pode conter um ou mais dos sinalizadores a seguir.

    

    | Sinalizador de depuração | Descrição                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | A combinação de teclas CTRL+ALT+SHIFT+TAB causará uma quebra de depuração no Winlogon.                                                                                               |
    | Erro          | Erros de impressão.                                                                                                                                                              |
    | Init           | Imprimir mensagens de inicialização e progresso.                                                                                                                                |
    | Notificar         | Imprimir mensagens do pacote de notificação.                                                                                                                                       |
    | SAS            | Imprima informações [*sobre notificações*](/windows/desktop/SecGloss/s-gly) de SAS (sequência de atenção segura). |
    | Estado          | Imprimir mensagens quando o Winlogon altera o estado.                                                                                                                                |
    | Tempo limite        | Imprimir mensagens quando um limite de tempo for definido ou um limite de tempo for atingido.                                                                                                        |
    | Trace          | Imprimir informações detalhadas de rastreamento.                                                                                                                                           |
    | Aviso           | Imprimir avisos.                                                                                                                                                            |

    

     

-   Para iniciar a versão verificada do Winlogon em um depurador, adicione a seguinte entrada ao Registro:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> Você deve usar o Windows NTSD (depurador simbólico) para depurar o Winlogon.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Carregando e executando uma DLL DE LTD](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funções de exportação DEAM](authentication-functions.md)
</dt> <dt>

[Estruturas DE FEDERAÇÃO](authentication-structures.md)
</dt> <dt>

[Funções DEIS dos Serviços de Terminal](terminal-services-gina-functions.md)
</dt> </dl>

 

 
