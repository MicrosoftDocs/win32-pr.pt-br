---
title: Movimentação de módulo
description: Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliotecas de vínculo dinâmico
- bibliotecas de vínculo dinâmico, enumerando DLLs
- enumerando
- Enumerando, DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084600"
---
# <a name="module-walking"></a>Movimentação de módulo

Um instantâneo que inclui a lista de módulos para um processo especificado contém informações sobre cada módulo, arquivo executável ou DLL (biblioteca de vínculo dinâmico), usado pelo processo especificado. Você pode recuperar informações para o primeiro módulo na lista usando a função [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . Depois de recuperar o primeiro módulo na lista, você pode recuperar informações para os módulos subsequentes na lista usando a função [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** e **Module32Next** preenchem uma estrutura [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) com informações sobre o módulo.

Você pode recuperar um código de status de erro estendido para [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) e [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) usando a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> O identificador de módulo, que é especificado no membro **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), só tem significado no Windows de 16 bits.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atravessando a lista de módulos](traversing-the-module-list.md)
</dt> </dl>

 

 