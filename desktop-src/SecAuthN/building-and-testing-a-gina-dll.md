---
description: Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de cabeçalho Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Criando e testando uma DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298058"
---
# <a name="building-and-testing-a-gina-dll"></a>Criando e testando uma DLL GINA

Todas as funções, protótipos, estruturas e constantes são definidas no arquivo de cabeçalho Winwlx. h.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Para testar uma dll [*Gina*](/windows/desktop/SecGloss/g-gly) , use o Winlogon.exe de uma versão verificada do sistema operacional, que está disponível com o Microsoft Windows Driver Development Kit (DDK). A versão verificada do [*Winlogon*](/windows/desktop/SecGloss/w-gly) dá suporte à depuração de ginas da seguinte maneira:

-   Você pode usar a sintaxe a seguir para criar uma seção em Win.ini para especificar opções de depuração do Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Se especificado, o **logfile** deverá conter o nome totalmente qualificado do arquivo que será usado para registrar informações de depuração. Se o arquivo não existir, ele será criado.

    As opções **DebugFlags** especificam quais tipos de informações de depuração gravar no arquivo de log ou depurador. **DebugFlags** pode conter um ou mais dos sinalizadores a seguir.

    

    | Sinalizador de depuração | Descrição                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | A combinação de teclas CTRL + ALT + SHIFT + TAB causará uma interrupção de depuração no Winlogon.                                                                                               |
    | Erro          | Erros de impressão.                                                                                                                                                              |
    | Init           | Imprimir mensagens de inicialização e progresso.                                                                                                                                |
    | Notificar         | Imprimir mensagens do pacote de notificação.                                                                                                                                       |
    | SAS            | Imprimir informações sobre notificações de [*sequência de atenção segura*](/windows/desktop/SecGloss/s-gly) (SAS). |
    | Estado          | Imprimir mensagens quando o Winlogon mudar de estado.                                                                                                                                |
    | Tempo limite        | Imprimir mensagens quando um limite de tempo for definido ou um limite de tempo for atingido.                                                                                                        |
    | Trace          | Imprimir informações de rastreamento detalhado.                                                                                                                                           |
    | Aviso           | Imprimir avisos.                                                                                                                                                            |

    

     

-   Para iniciar a versão verificada do Winlogon em um depurador, adicione a seguinte entrada ao registro:

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
> Você deve usar o depurador simbólico do Windows (NTSD) para depurar o Winlogon.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Carregando e executando uma DLL GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funções de exportação GINA](authentication-functions.md)
</dt> <dt>

[Estruturas GINA](authentication-structures.md)
</dt> <dt>

[Funções de GINA de serviços de terminal](terminal-services-gina-functions.md)
</dt> </dl>

 

 
