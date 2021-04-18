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
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="e4d22-103">Removendo nomes e descrições de contadores do registro</span><span class="sxs-lookup"><span data-stu-id="e4d22-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="e4d22-104">A ferramenta **Unlodctr** remove as entradas do registro criadas por **lodctr**.</span><span class="sxs-lookup"><span data-stu-id="e4d22-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="e4d22-105">O nome do aplicativo que você passa para **Unlodctr** deve corresponder ao [nome da chave do aplicativo](creating-the-applications-performance-key.md) que você criou na chave de **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="e4d22-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="e4d22-106">Para obter detalhes sobre como executar o **Unlodctr** , consulte o centro de ajuda e suporte.</span><span class="sxs-lookup"><span data-stu-id="e4d22-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="e4d22-107">Usando o Unlodctr</span><span class="sxs-lookup"><span data-stu-id="e4d22-107">Using unlodctr</span></span>

<span data-ttu-id="e4d22-108">A ferramenta **Unlodctr** pesquisa o primeiro e último contador e os valores de índice da ajuda usando os valores de registro nomeados na chave de **desempenho** do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4d22-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="e4d22-109">A ferramenta **Unlodctr** usa o intervalo de valores de índice para remover o texto dos **contadores** e os valores de **ajuda** para cada identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="e4d22-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="e4d22-110">Usando os valores de índice, o **Unlodctr** faz as seguintes alterações no registro.</span><span class="sxs-lookup"><span data-stu-id="e4d22-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

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

<span data-ttu-id="e4d22-111">A ferramenta **Unlodctr** também remove os valores do **primeiro contador**, **último contador**, **primeiro ajuda**, **última ajuda** e **lista de objetos** da chave de **desempenho** do aplicativo localizada em **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *Application-Name* \\ **performance**.</span><span class="sxs-lookup"><span data-stu-id="e4d22-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="e4d22-112">A função de descarregamento de **Unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), é declarada em LoadPerf. h e exportada de Loadperf.dll.</span><span class="sxs-lookup"><span data-stu-id="e4d22-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="e4d22-113">Isso permite que você chame essa função diretamente do seu programa de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="e4d22-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



