---
title: Recuperando informações de status
description: Recuperando informações de status
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, recuperando status
- lojas online, recuperando status
- tipo 2 lojas online, recuperando status
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Recuperando status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636642"
---
# <a name="retrieving-status-information"></a><span data-ttu-id="901c1-113">Recuperando informações de status</span><span class="sxs-lookup"><span data-stu-id="901c1-113">Retrieving Status Information</span></span>

<span data-ttu-id="901c1-114">As informações de status são atualizadas usando o temporizador criado na função **init** .</span><span class="sxs-lookup"><span data-stu-id="901c1-114">Status information is updated using the timer created in the **Init** function.</span></span> <span data-ttu-id="901c1-115">Todo o status é atualizado usando o mesmo temporizador.</span><span class="sxs-lookup"><span data-stu-id="901c1-115">All status is updated using the same timer.</span></span> <span data-ttu-id="901c1-116">O nome da função para o evento de timer é **OnTimer**.</span><span class="sxs-lookup"><span data-stu-id="901c1-116">The name of the function for the timer event is **OnTimer**.</span></span>

<span data-ttu-id="901c1-117">**OnTimer** determina as informações a serem exibidas com base na seleção de usuário, que é armazenada na variável global chamada g \_ oCurrentDLItem.</span><span class="sxs-lookup"><span data-stu-id="901c1-117">**OnTimer** determines the information to display based upon the user selection, which is stored in the global variable named g\_oCurrentDLItem.</span></span> <span data-ttu-id="901c1-118">A função primeiro testa se os valores de tamanho ou de progresso são válidos e cria uma cadeia de caracteres para cada caso.</span><span class="sxs-lookup"><span data-stu-id="901c1-118">The function first tests whether the size or progress values are valid and creates a string for each case.</span></span>


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



<span data-ttu-id="901c1-119">Se um valor for válido, a cadeia de caracteres representará a contagem de bytes.</span><span class="sxs-lookup"><span data-stu-id="901c1-119">If a value is valid, the string represents the byte count.</span></span> <span data-ttu-id="901c1-120">Se o valor não for válido, como-1, a cadeia de caracteres fornecerá uma mensagem para informar ao usuário que as informações ainda não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="901c1-120">If the value is not valid, such as -1, the string provides a message to inform the user that the information is not yet available.</span></span>

<span data-ttu-id="901c1-121">Em seguida, um bloco de **opção** determina se o download do item selecionado foi concluído ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="901c1-121">Next, a **switch** block determines whether the download for the selected item is completed or canceled.</span></span> <span data-ttu-id="901c1-122">Se qualquer um dos casos for verdadeiro, o valor do tamanho ou do progresso das variáveis será atualizado de acordo.</span><span class="sxs-lookup"><span data-stu-id="901c1-122">If either case is true, the value of the variables Size or Progress is updated accordingly.</span></span>


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



<span data-ttu-id="901c1-123">Por fim, as informações de status são exibidas no elemento DIV chamado dlstate.</span><span class="sxs-lookup"><span data-stu-id="901c1-123">Finally, the status information is displayed in the DIV element named dlstate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="901c1-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="901c1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="901c1-125">**Usando o Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="901c1-125">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




