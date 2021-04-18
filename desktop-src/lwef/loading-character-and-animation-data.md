---
title: Carregando dados de caractere e animação
description: Carregando dados de caractere e animação
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789219"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="9977a-103">Carregando dados de caractere e animação</span><span class="sxs-lookup"><span data-stu-id="9977a-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="9977a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9977a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9977a-105">Depois de ter um ponteiro para a interface [**IAgentEx**](iagentex.md) , você pode usar o método [**Load**](load-method.md) para carregar um caractere e recuperar sua interface [**IAgentCharacterEx**](iagentcharacterex.md) .</span><span class="sxs-lookup"><span data-stu-id="9977a-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="9977a-106">Há três possibilidades diferentes para o caminho de carga de um caractere.</span><span class="sxs-lookup"><span data-stu-id="9977a-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="9977a-107">O primeiro é compatível com o Microsoft Agent 1,5, em que o caminho especificado é o caminho completo e o nome do arquivo de um caractere.</span><span class="sxs-lookup"><span data-stu-id="9977a-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="9977a-108">A segunda possibilidade é especificar apenas o nome do arquivo, nesse caso, o Agent examina seu diretório chars.</span><span class="sxs-lookup"><span data-stu-id="9977a-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="9977a-109">A última possibilidade é fornecer um parâmetro VARIANT vazio que faz com que o caractere padrão seja carregado.</span><span class="sxs-lookup"><span data-stu-id="9977a-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="9977a-110">Você pode usar essa interface para acessar os métodos do caractere:</span><span class="sxs-lookup"><span data-stu-id="9977a-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="9977a-111">Quando você não precisar mais dos serviços do Microsoft Agent, como quando o aplicativo cliente é desligado, libere suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="9977a-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="9977a-112">Observe que a liberação da interface de caracteres não descarrega o caractere.</span><span class="sxs-lookup"><span data-stu-id="9977a-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="9977a-113">Chame o método [**Unload**](unload-method.md) para fazer isso antes de liberar a interface [**IAgentEx**](iagentex.md) :</span><span class="sxs-lookup"><span data-stu-id="9977a-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




