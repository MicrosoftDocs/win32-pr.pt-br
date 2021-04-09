---
description: Integralmente para testar e depurar suas implementações de manipulador de protocolo é entender como os manipuladores de protocolo são iniciados.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Depuração de manipuladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090054"
---
# <a name="debugging-protocol-handlers"></a>Depuração de manipuladores de protocolo

Integralmente para testar e depurar suas implementações de manipulador de protocolo é entender como os manipuladores de protocolo são iniciados.

Este tópico é organizado da seguinte maneira:

-   [Sobre a depuração de manipuladores de protocolo](#about-debugging-protocol-handlers)
-   [Configurando a depuração](#setting-up-debugging)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-debugging-protocol-handlers"></a>Sobre a depuração de manipuladores de protocolo

O processo SearchIndexer (searchindexer.exe) inicia uma cópia do processo SearchProtocolHost (SearchProtocolHost.exe) no contexto do sistema e outra cópia no contexto do usuário. Em seguida, os manipuladores de protocolo são carregados no processo SearchProtocolHost, conforme necessário. Eles não são descarregados até que o serviço de pesquisa seja interrompido. A mesma instância de um manipulador de protocolo é reutilizada quantas vezes o serviço estiver em execução.

Os processos SearchIndexer e SearchProtocolHost se comunicam frequentemente durante a indexação. Se você pausar ou parar o processo SearchProtocolHost para depurar, o SearchIndexer abrirá um novo processo SearchProtocolHost, invalidando a sessão de depuração. Além disso, se você anexar o depurador diretamente ao processo SearchProtocolHost, poderá interromper o identificador-herança de searchindexer.exe para searchprotocolhost.exe e os dois processos não poderão se comunicar.

Para evitar esses problemas, você precisa notificar o serviço de pesquisa que está Depurando, e você precisa anexar o depurador ao processo SearchIndexer com instruções para depurar processos filho, conforme descrito a seguir.

## <a name="setting-up-debugging"></a>Configurando a depuração

Siga estas etapas para configurar a depuração para o manipulador de protocolo.

1.  Notifique o serviço de pesquisa que você está depurando definindo o valor de DebugFilters como 1 no registro:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  Anexar um depurador usando a chave do registro de opções de execução do arquivo de imagem:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    As opções para um depurador de exemplo são descritas na tabela a seguir.

    

    **Exemplo usando o depurador do depurador do NTSD**   *= C: \\ depuradores \\ntsd.exe-odGx-C: "sXe LD mydll.dll; g"*<br/>

3.  Reinicie searchindexer.exe no depurador usando compmgmt. msc, Services. msc ou uma janela de comando com comandos semelhantes ao seguinte:
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

Para distinguir entre um processo SearchProtocolHost em execução no contexto do sistema e outro em execução no contexto do usuário, você pode examinar as cadeias de caracteres do ambiente. Com ntsd.exe, por exemplo, você pode usar o comando de extensão **! PEB** para exibir uma exibição formatada das informações no bloco de ambiente do processo (PEB).

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como criar manipuladores, consulte [registrando extensões de shell](../shell/reg-shell-exts.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt><a href="-search-3x-wds-phaddins.md">Manipuladores de protocolos de desenvolvimento</a></dt> <dt>**conceituados**</dt> que <dt><a href="-search-3x-wds-extidx-prot-implementing.md">compreendem manipuladores de protocolo</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">notificando o índice das alterações</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">adicionando ícones e menus de contexto</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">exemplo de código: extensões de Shell para manipuladores de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">criando um conector de pesquisa para um manipulador de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Instalando e Registrando manipuladores de protocolo</a></dt> </dl>

 

 
