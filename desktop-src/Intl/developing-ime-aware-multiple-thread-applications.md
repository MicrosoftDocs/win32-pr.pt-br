---
description: O IMM inclui a verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto de método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desenvolvendo IME-Aware aplicativos de vários threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782800"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Desenvolvendo IME-Aware aplicativos de vários threads

O IMM inclui a verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto de método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND). Se o thread não for o criador do identificador, a função chamada IMM falhará e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ \_ acesso inválido.

> [!Note]  
> A arquitetura atual do IMM não fornece um recurso de sincronização para acesso aos identificadores do IMM.

 

Para usar a verificação de identificação de thread, seus aplicativos devem aderir às seguintes diretrizes:

-   Um thread não deve acessar o contexto de entrada criado por outro thread.
-   Um thread não deve associar um contexto de entrada a uma janela criada por outro thread, e vice-versa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 
