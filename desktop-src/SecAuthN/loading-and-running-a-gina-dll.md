---
description: O Windows carrega e executa a DLL padrão do Microsoft GINA (MSGina.dll). Para carregar uma GINA diferente, você deve alterar um valor de chave do registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Carregando e executando uma DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747510"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="eaa06-104">Carregando e executando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="eaa06-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="eaa06-105">O Windows carrega e executa a DLL padrão do Microsoft GINA (MSGina.dll).</span><span class="sxs-lookup"><span data-stu-id="eaa06-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="eaa06-106">Para carregar uma [*Gina*](../secgloss/g-gly.md)diferente, você deve alterar o seguinte valor de chave do registro:</span><span class="sxs-lookup"><span data-stu-id="eaa06-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="eaa06-107">Se o valor da chave GinaDLL estiver presente, ele deverá conter o nome de uma DLL GINA, que o [*Winlogon*](../secgloss/w-gly.md) carregará e usará.</span><span class="sxs-lookup"><span data-stu-id="eaa06-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaa06-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eaa06-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa06-109">Criando e testando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="eaa06-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="eaa06-110">Funções de exportação GINA</span><span class="sxs-lookup"><span data-stu-id="eaa06-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="eaa06-111">Estruturas GINA</span><span class="sxs-lookup"><span data-stu-id="eaa06-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="eaa06-112">Funções de GINA de serviços de terminal</span><span class="sxs-lookup"><span data-stu-id="eaa06-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
