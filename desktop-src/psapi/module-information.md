---
title: Informações do módulo
description: Um módulo é um arquivo executável ou DLL.
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366121"
---
# <a name="module-information"></a>Informações do módulo

Um *módulo* é um arquivo executável ou dll. Cada processo consiste em um ou mais módulos. Você pode recuperar a lista de identificadores de módulo para um processo chamando a função [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) . Essa função preenche uma matriz de valores **HMODULE** com as alças do módulo para o processo especificado. O primeiro módulo é o arquivo executável. Lembre-se de que esses identificadores de módulo são mais prováveis de algum outro processo, portanto, você não pode usá-los com funções como [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea). No entanto, você pode usar as [funções psapi](psapi-functions.md) para obter informações sobre um módulo de outro processo.

O procedimento a seguir descreve como obter informações de módulo de outro processo.

**Para obter informações de módulo de outro processo**

1.  Chame a função [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) . Essa função usa um identificador de processo e um identificador de módulo como entrada e preenche um buffer com o nome base de um módulo (por exemplo, Kernel32.dll). Uma função relacionada, [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa), usa os mesmos parâmetros como entrada, mas retorna o caminho completo para o módulo (por exemplo, C: \\ Windows \\ System32 \\Kernel32.dll).
2.  Chame a função [**GetModuleInformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) . Essa função usa um identificador de processo e um identificador de módulo e preenche uma estrutura [**ModuleInfo**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) com o endereço de carregamento do módulo, o tamanho do espaço de endereço linear que ele ocupa e um ponteiro para seu ponto de entrada.

Se um aplicativo exigir informações de módulo para o processo atual, ele deverá usar a função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) em vez das funções de módulo psapi. Isso ajuda o desempenho do aplicativo de duas maneiras: a função **GetModuleFileName** é mais eficiente do que as funções do módulo psapi, e um aplicativo pode evitar o carregamento de psapi.dll se não usar nenhuma função psapi.

As funções [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) e [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) são projetadas principalmente para uso por depuradores e aplicativos semelhantes que devem extrair informações de módulo de outro processo. Se a lista de módulos no processo de destino estiver corrompida ou ainda não tiver sido inicializada, ou se a lista de módulos for alterada durante a chamada de função como resultado de DLLs sendo carregadas ou descarregadas, essas funções poderão falhar ou retornar informações incorretas.

 

 