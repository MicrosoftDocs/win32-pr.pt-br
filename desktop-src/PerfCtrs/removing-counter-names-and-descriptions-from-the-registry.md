---
description: A ferramenta unlodctr remove as entradas do Registro criadas pelo lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Removendo nomes de contadores e descrições do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c086520f1fb261a0b9850c03f2aee28065a03ee514df277fbf1cae602deed6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962346"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Removendo nomes de contadores e descrições do Registro

A **ferramenta unlodctr** remove as entradas do Registro criadas por **lodctr**. O nome do aplicativo que você passa para **unlodctr deve** corresponder ao nome da chave do aplicativo [que](creating-the-applications-performance-key.md) você criou na chave **Serviços.** Para obter detalhes sobre como **executar unlodctr,** consulte, Centro de Ajuda e Suporte.

## <a name="using-unlodctr"></a>Usando unlodctr

A **ferramenta unlodctr** procura o primeiro e o último contador e ajuda a indexar valores usando os valores de registro nomeados como na chave de desempenho **do** aplicativo. A **ferramenta unlodctr** usa o intervalo de valores de índice para remover o texto dos valores de **Contadores** e **Ajuda** para cada identificador de idioma.

Usando os valores de índice, **unlodctr** faz as seguintes alterações no Registro.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

A **ferramenta unlodctr** também remove os valores First **Counter**, Last **Counter**, First  **Help**, **Last Help** e **Object List** da chave de desempenho do aplicativo localizada em **HKEY LOCAL \_ \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ *application-name* \\ **Performance**.

> [!Note]  
> A função de descarregamento **de unlodctr,** [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), é declarada em Loadperf.h e exportada de Loadperf.dll. Isso permite que você chame essa função diretamente do programa de desinstalação.

 

 

 



