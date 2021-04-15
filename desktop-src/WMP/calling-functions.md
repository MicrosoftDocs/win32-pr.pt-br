---
title: Chamando Funções
description: Chamando Funções
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Capas do Windows Media Player, chamando funções no JScript
- capas, chamando funções no JScript
- chamando funções no JScript
- Arquivos JScript para capas, chamando funções
- Capas do Windows Media Player, atributo scriptfile no JScript
- Skins, atributo scriptfile no JScript
- atributos, scriptfile em JScript
- atributo scriptfile no JScript
- Arquivos JScript para capas, atributo scriptfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498807"
---
# <a name="calling-functions"></a><span data-ttu-id="5d4e8-112">Chamando Funções</span><span class="sxs-lookup"><span data-stu-id="5d4e8-112">Calling Functions</span></span>

<span data-ttu-id="5d4e8-113">Se você precisar chamar mais de algumas linhas de código, poderá carregar um arquivo de script usando o atributo **scriptfile** do elemento **View** e chamar as funções no script.</span><span class="sxs-lookup"><span data-stu-id="5d4e8-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="5d4e8-114">Você pode carregar mais de um arquivo por exibição:</span><span class="sxs-lookup"><span data-stu-id="5d4e8-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="5d4e8-115">Depois que os arquivos de script são carregados, você pode chamar funções neles de dentro de sua seção de exibição.</span><span class="sxs-lookup"><span data-stu-id="5d4e8-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="5d4e8-116">Por exemplo, para chamar uma função chamada *MyFunction* quando algo é clicado, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5d4e8-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="5d4e8-117">Se você tiver mais de uma exibição, somente as funções em arquivos carregados no modo de exibição atual estarão disponíveis para o código XML e JScript em execução com a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="5d4e8-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="5d4e8-118">Os arquivos carregados em outras exibições não estão no escopo com a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="5d4e8-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5d4e8-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d4e8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d4e8-120">**Usando o JScript**</span><span class="sxs-lookup"><span data-stu-id="5d4e8-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




