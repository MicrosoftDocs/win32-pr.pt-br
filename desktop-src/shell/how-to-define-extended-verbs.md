---
description: Você pode usar o registro para definir um ou mais verbos estendidos. Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto ao pressionar a tecla SHIFT.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Como definir verbos estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967907"
---
# <a name="how-to-define-extended-verbs"></a><span data-ttu-id="f654f-104">Como definir verbos estendidos</span><span class="sxs-lookup"><span data-stu-id="f654f-104">How to Define Extended Verbs</span></span>

<span data-ttu-id="f654f-105">Você pode usar o registro para definir um ou mais verbos estendidos.</span><span class="sxs-lookup"><span data-stu-id="f654f-105">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="f654f-106">Os comandos associados serão exibidos somente quando o usuário clicar com o botão direito do mouse em um objeto ao pressionar a tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="f654f-106">The associated commands will be displayed only when the user right-clicks an object while pressing the SHIFT key.</span></span>

## <a name="instructions"></a><span data-ttu-id="f654f-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="f654f-107">Instructions</span></span>


<span data-ttu-id="f654f-108">Para definir um verbo como estendido, basta adicionar um valor de **\_ sz reg** "estendido" à subchave do verbo.</span><span class="sxs-lookup"><span data-stu-id="f654f-108">To define a verb as extended, simply add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="f654f-109">O valor não deve ter nenhum dado associado a ele.</span><span class="sxs-lookup"><span data-stu-id="f654f-109">The value should not have any data associated with it.</span></span> <span data-ttu-id="f654f-110">A seguinte entrada de registro de exemplo mostra o exemplo da seção anterior, com "doit" definido como um verbo estendido.</span><span class="sxs-lookup"><span data-stu-id="f654f-110">The following sample registry entry shows the example from the previous section, with "doit" defined as an extended verb.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



