---
title: Listas de heap e movimentação de heap
description: Um instantâneo que inclui a lista de heaps para um processo especificado contém informações de identificação para cada heap associado ao processo especificado e informações detalhadas sobre cada heap.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5a9b8d30e2de1bf5ab37de03fdcb3fde663417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641267"
---
# <a name="heap-lists-and-heap-walking"></a>Listas de heap e movimentação de heap

Um instantâneo que inclui a lista de heaps para um processo especificado contém informações de identificação para cada heap associado ao processo especificado e informações detalhadas sobre cada heap. Você pode recuperar um identificador para o primeiro heap da lista de heaps usando a função [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) . Depois de recuperar o primeiro heap na lista, você pode atravessar a lista de heap para heaps subsequentes associados ao processo usando a função [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . **Heap32ListFirst** e **Heap32ListNext** preenchem uma estrutura [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) com o identificador do processo, o identificador de heap e os sinalizadores que descrevem o heap.

Você pode recuperar informações sobre o primeiro bloco de um heap usando a função [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) . Depois de recuperar o primeiro bloco de um heap, você pode recuperar informações sobre blocos subsequentes do mesmo heap usando a função [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) . **Heap32First** e **Heap32Next** preenchem uma estrutura [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) com informações para o bloco apropriado de um heap.

Você pode recuperar um código de status de erro estendido para [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)e [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> O identificador de heap, que é especificado no membro **th32HeapID** da estrutura [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) , tem significado apenas para as funções de ajuda da ferramenta. Ele não é um identificador, nem pode ser usado por outras funções.

 

 

 