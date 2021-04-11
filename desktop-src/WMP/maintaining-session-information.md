---
title: Mantendo informações da sessão
description: Mantendo informações da sessão
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, mantendo informações de sessão
- lojas online, mantendo informações de sessão
- Digite 2 lojas online, mantendo as informações da sessão
- Armazenamentos online do Windows Media Player, informações da sessão
- lojas online, informações da sessão
- Digite 2 lojas online, informações da sessão
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- mantendo informações da sessão
- informações da sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292859"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="aa16e-117">Mantendo informações da sessão</span><span class="sxs-lookup"><span data-stu-id="aa16e-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="aa16e-118">Como o exemplo armazena informações</span><span class="sxs-lookup"><span data-stu-id="aa16e-118">How the Sample Stores Information</span></span>

<span data-ttu-id="aa16e-119">A página da Web de exemplo mantém dados usando cookies.</span><span class="sxs-lookup"><span data-stu-id="aa16e-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="aa16e-120">Os cookies são simplesmente pares de nome/valor persistentes que o navegador da Web pode armazenar para você.</span><span class="sxs-lookup"><span data-stu-id="aa16e-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="aa16e-121">Quando a página da Web é fechada, a função de **desligamento** é executada.</span><span class="sxs-lookup"><span data-stu-id="aa16e-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="aa16e-122">**Shutdown** chama a função **SetPendingCookies**.</span><span class="sxs-lookup"><span data-stu-id="aa16e-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="aa16e-123">Essa função faz um loop pela lista de coleta de download, armazenada na caixa de listagem suspensa chamada selDLC.</span><span class="sxs-lookup"><span data-stu-id="aa16e-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="aa16e-124">Se uma coleção de download contiver itens incompletos, a função chamará o método **SetCookie**, passando um nome e um valor.</span><span class="sxs-lookup"><span data-stu-id="aa16e-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="aa16e-125">A cadeia de caracteres de nome é determinada acrescentando um valor inteiro a um valor constante, **WMPDLC**, que é armazenado na variável chamada g \_ sPreCookie.</span><span class="sxs-lookup"><span data-stu-id="aa16e-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="aa16e-126">Por exemplo, para a terceira coleção de download pendente, o nome do cookie seria "WMPDLC2", porque o mecanismo de contagem é baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="aa16e-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="aa16e-127">À medida que cada cookie é criado, a função incrementa a variável global g \_ pendente para manter uma contagem de downloads pendentes.</span><span class="sxs-lookup"><span data-stu-id="aa16e-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="aa16e-128">O código é reproduzido aqui para sua conveniência:</span><span class="sxs-lookup"><span data-stu-id="aa16e-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="aa16e-129">**IsDLCComplete** é uma função auxiliar que simplesmente executa loops em cada item de download da coleção de download para determinar se algum item está pendente.</span><span class="sxs-lookup"><span data-stu-id="aa16e-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="aa16e-130">Se houver um item pendente, a função retornará false.</span><span class="sxs-lookup"><span data-stu-id="aa16e-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="aa16e-131">**SetCookie** é a função que cria o cookie.</span><span class="sxs-lookup"><span data-stu-id="aa16e-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="aa16e-132">Quando **SetPendingCookies** retorna, o **desligamento** cria o cookie de contagem, que armazena o valor da variável g \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="aa16e-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="aa16e-133">Esse valor é importante porque a página da Web precisa de uma maneira de determinar quantos cookies serão recuperados quando recarregados.</span><span class="sxs-lookup"><span data-stu-id="aa16e-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="aa16e-134">O nome do cookie de contagem é armazenado na variável chamada g \_ sCountCookie.</span><span class="sxs-lookup"><span data-stu-id="aa16e-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="aa16e-135">Como o exemplo recupera informações</span><span class="sxs-lookup"><span data-stu-id="aa16e-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="aa16e-136">Quando a página da Web é carregada, a função **init** é executada.</span><span class="sxs-lookup"><span data-stu-id="aa16e-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="aa16e-137">Primeiro, a função chama **GetPendingDlCount** para recuperar o cookie de contagem.</span><span class="sxs-lookup"><span data-stu-id="aa16e-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="aa16e-138">Em seguida, ele armazena esse valor na variável chamada g \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="aa16e-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="aa16e-139">Em seguida, ele chama a função **PopulateDLList** para recuperar cada cookie de sessão de download e adiciona seu identificador à caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="aa16e-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="aa16e-140">Este é o código para essa função:</span><span class="sxs-lookup"><span data-stu-id="aa16e-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="aa16e-141">A função **clearlist** remove todos os itens da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="aa16e-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="aa16e-142">Em seguida, a função entra em um loop.</span><span class="sxs-lookup"><span data-stu-id="aa16e-142">The function then enters a loop.</span></span> <span data-ttu-id="aa16e-143">Cada nome de cookie é criado como uma cadeia de caracteres e, em seguida, o cookie é recuperado chamando a função auxiliar **GetCookie**.</span><span class="sxs-lookup"><span data-stu-id="aa16e-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="aa16e-144">Depois de recuperados, o cookie é excluído chamando **DelCookie**.</span><span class="sxs-lookup"><span data-stu-id="aa16e-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="aa16e-145">Se o cookie tiver um valor, o valor será adicionado à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="aa16e-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="aa16e-146">Essa ação inicia o evento **onChange** para a lista selDLC, que, por sua vez, chama a função de manipulador denominada **OnSelectDLC**.</span><span class="sxs-lookup"><span data-stu-id="aa16e-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="aa16e-147">Essa é a mesma função que é executada quando o usuário seleciona uma coleção de download; é o código que preenche a caixa de listagem baixar item.</span><span class="sxs-lookup"><span data-stu-id="aa16e-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa16e-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa16e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa16e-149">**Usando o Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="aa16e-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




