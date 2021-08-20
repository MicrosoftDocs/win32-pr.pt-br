---
title: Módulo de ida e volta
description: Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliotecas de vínculo dinâmico
- bibliotecas de vínculo dinâmico, enumerando DLLs
- enumerando
- enumerando,DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61e72fcdbcae52a78e62465b12845077572b6b4669e1b0744c26d50ddfd2a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126486"
---
# <a name="module-walking"></a>Módulo de ida e volta

Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado. Você pode recuperar informações para o primeiro módulo na lista usando a [**função Module32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) Depois de recuperar o primeiro módulo na lista, você pode recuperar informações para módulos subsequentes na lista usando a [**função Module32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) **Module32First** e **Module32Next** preencham uma estrutura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) com informações sobre o módulo.

Você pode recuperar um código de status de erro estendido [**para Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) usando a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> O identificador do módulo, que é especificado no membro **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), só tem significado em 16 bits Windows.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Percorrendo a lista de módulos](traversing-the-module-list.md)
</dt> </dl>

 

 