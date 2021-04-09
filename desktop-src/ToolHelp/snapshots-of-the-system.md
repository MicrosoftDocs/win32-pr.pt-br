---
title: Instantâneos do sistema
description: Os instantâneos estão no centro das funções de ajuda da ferramenta. Um instantâneo é uma cópia somente leitura do estado atual de uma ou mais das listas a seguir que residem em processos de memória do sistema, threads, módulos e heaps.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823863"
---
# <a name="snapshots-of-the-system"></a>Instantâneos do sistema

Os instantâneos estão no centro das funções de ajuda da ferramenta. Um instantâneo é uma cópia somente leitura do estado atual de uma ou mais das listas a seguir que residem na memória do sistema: processos, threads, módulos e heaps.

Processos que usam funções de ajuda da ferramenta acessam essas listas de instantâneos em vez de diretamente do sistema operacional. As listas na alteração da memória do sistema quando os processos são iniciados e encerrados, os threads são criados e destruídos, os módulos executáveis são carregados e descarregados da memória do sistema e os heaps são criados e destruídos. O uso de informações de um instantâneo impede inconsistências. Caso contrário, as alterações em uma lista podem fazer com que um thread percorra incorretamente a lista ou cause uma violação de acesso (uma falha de GP). Por exemplo, se um aplicativo atravessa a lista de threads enquanto outros threads são criados ou encerrados, as informações que o aplicativo está usando para atravessar a lista de threads podem se tornar desatualizadas e podem causar um erro para que o aplicativo percorra a lista.

Para tirar um instantâneo da memória do sistema, use a função [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) . Você pode controlar o conteúdo de um instantâneo especificando um ou mais dos seguintes valores ao chamar essa função:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Os valores **TH32CS \_ SNAPHEAPLIST** e **TH32CS \_ SNAPMODULE** são específicos do processo. Quando esses valores são especificados, as listas de heap e módulo do processo especificado são incluídas no instantâneo. Se você especificar zero como o identificador do processo, o processo atual será usado. O valor de **TH32CS \_ SNAPTHREAD** sempre cria um instantâneo em todo o sistema, mesmo se um identificador de processo for passado para [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).

Para enumerar o estado de heap ou de módulo para todos os processos, especifique o valor de **\_ SNAPALL TH32CS** e o identificador de processo do processo atual. Em seguida, para cada processo adicional no instantâneo, chame [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) novamente, especificando seu identificador de processo e o valor **TH32CS \_ SNAPHEAPLIST** ou **TH32CS \_ SNAPMODULE** .

Você pode recuperar um código de status de erro estendido para [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Quando o processo terminar de usar um instantâneo, destrua-o usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se você não destruir um instantâneo, o processo irá vazar memória até que ele saia, quando o sistema recuperar a memória.

> [!Note]  
> O identificador de instantâneo funciona como um identificador de arquivo e está sujeito às mesmas regras em relação aos processos e threads nos quais ele pode ser usado. Para especificar que o identificador é herdável, crie o instantâneo usando o valor de **\_ herança TH32CS** .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fazendo um instantâneo e exibindo processos](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 