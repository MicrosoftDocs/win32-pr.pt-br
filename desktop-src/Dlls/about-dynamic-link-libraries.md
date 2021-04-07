---
description: A vinculação dinâmica permite que um módulo inclua apenas as informações necessárias para localizar uma função DLL exportada no tempo de carregamento ou em tempo de execução.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Sobre bibliotecas de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdb24048e17e9164aaf39d0ab337aea33576c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827517"
---
# <a name="about-dynamic-link-libraries"></a>Sobre bibliotecas de Dynamic-Link

A vinculação dinâmica permite que um módulo inclua apenas as informações necessárias para localizar uma função DLL exportada no tempo de carregamento ou em tempo de execução. A vinculação dinâmica difere da vinculação estática mais familiar, na qual o vinculador copia o código de uma função de biblioteca em cada módulo que a chama.

## <a name="types-of-dynamic-linking"></a>Tipos de vinculação dinâmica

Há dois métodos para chamar uma função em uma DLL:

-   Em *vinculação dinâmica em tempo de carregamento*, um módulo faz chamadas explícitas para funções de dll exportadas como se fossem funções locais. Isso exige que você vincule o módulo com a biblioteca de importação para a DLL que contém as funções. Uma biblioteca de importação fornece ao sistema as informações necessárias para carregar a DLL e localizar as funções de DLL exportadas quando o aplicativo é carregado.
-   Em *vinculação dinâmica em tempo de execução*, um módulo usa a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) para carregar a dll em tempo de execução. Depois que a DLL é carregada, o módulo chama a função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter os endereços das funções DLL exportadas. O módulo chama as funções de DLL exportadas usando os ponteiros de função retornados por **GetProcAddress**. Isso elimina a necessidade de uma biblioteca de importação.

## <a name="dlls-and-memory-management"></a>DLLs e gerenciamento de memória

Cada processo que carrega a DLL a mapeia em seu espaço de endereço virtual. Depois que o processo carrega a DLL em seu endereço virtual, ele pode chamar as funções de DLL exportadas.

O sistema mantém uma contagem de referência por processo para cada DLL. Quando um thread carrega a DLL, a contagem de referência é incrementada em uma. Quando o processo é encerrado, ou quando a contagem de referência se torna zero (somente vinculação dinâmica em tempo de execução), a DLL é descarregada do espaço de endereço virtual do processo.

Como qualquer outra função, uma função DLL exportada é executada no contexto do thread que a chama. Portanto, as seguintes condições se aplicam:

-   Os threads do processo que chamou a DLL podem usar identificadores abertos por uma função de DLL. Da mesma forma, os identificadores abertos por qualquer thread do processo de chamada podem ser usados na função DLL.
-   A DLL usa a pilha do thread de chamada e o espaço de endereço virtual do processo de chamada.
-   A DLL aloca memória do espaço de endereço virtual do processo de chamada.

Para obter mais informações sobre DLLs, consulte os seguintes tópicos:

-   [Vantagens da vinculação dinâmica](advantages-of-dynamic-linking.md)
-   [Criação de biblioteca de vínculo dinâmico](dynamic-link-library-creation.md)
-   [Função de Entry-Point de biblioteca de vínculo dinâmico](dynamic-link-library-entry-point-function.md)
-   [Vinculação dinâmica em tempo de carregamento](load-time-dynamic-linking.md)
-   [Vinculação dinâmica em tempo de execução](run-time-dynamic-linking.md)
-   [Ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md)
-   [Dados da biblioteca de vínculo dinâmico](dynamic-link-library-data.md)
-   [Redirecionamento de biblioteca de vínculo dinâmico](dynamic-link-library-redirection.md)
-   [Atualizações da biblioteca de vínculo dinâmico](dynamic-link-library-updates.md)
-   [Segurança da biblioteca de vínculo dinâmico](dynamic-link-library-security.md)
-   [AppInit DLLs e inicialização segura](secure-boot-and-appinit-dlls.md)

 

 
