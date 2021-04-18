---
description: A ferramenta Unlodctr remove as entradas do registro criadas por Lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Removendo nomes e descrições de contadores do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780485"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Removendo nomes e descrições de contadores do registro

A ferramenta **Unlodctr** remove as entradas do registro criadas por **lodctr**. O nome do aplicativo que você passa para **Unlodctr** deve corresponder ao [nome da chave do aplicativo](creating-the-applications-performance-key.md) que você criou na chave de **Serviços** . Para obter detalhes sobre como executar o **Unlodctr** , consulte o centro de ajuda e suporte.

## <a name="using-unlodctr"></a>Usando o Unlodctr

A ferramenta **Unlodctr** pesquisa o primeiro e último contador e os valores de índice da ajuda usando os valores de registro nomeados na chave de **desempenho** do seu aplicativo. A ferramenta **Unlodctr** usa o intervalo de valores de índice para remover o texto dos **contadores** e os valores de **ajuda** para cada identificador de idioma.

Usando os valores de índice, o **Unlodctr** faz as seguintes alterações no registro.

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

A ferramenta **Unlodctr** também remove os valores do **primeiro contador**, **último contador**, **primeiro ajuda**, **última ajuda** e **lista de objetos** da chave de **desempenho** do aplicativo localizada em **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.

> [!Note]  
> A função de descarregamento de **Unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), é declarada em LoadPerf. h e exportada de Loadperf.dll. Isso permite que você chame essa função diretamente do seu programa de desinstalação.

 

 

 



