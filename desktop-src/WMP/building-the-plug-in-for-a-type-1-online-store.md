---
title: Criando o plug-in para uma loja online tipo 1
description: Criando o plug-in para uma loja online tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Lojas online do Windows Media Player, criando plug-ins
- lojas online, criando plug-ins
- Digite 1 lojas online, criando plug-ins
- Lojas online do Windows Media Player, interface IWMPContentPartner
- lojas online, interface IWMPContentPartner
- Digite 1 lojas online, interface IWMPContentPartner
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, interface IWMPContentPartner
- plug-ins, compilando
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, interface IWMPContentPartner
- Plug-ins do Windows Media Player, compilando
- IWMPContentPartner
- Criando plug-ins, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105794510"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="75175-124">Criando o plug-in para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="75175-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="75175-125">Um repositório online tipo 1 deve fornecer um plug-in que implementa a interface [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="75175-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="75175-126">O plug-in é executado em um processo separado do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="75175-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="75175-127">As etapas para criar um plug-in que executa fora do processo são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="75175-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="75175-128">Escreva seu plug-in como se fosse um servidor COM em processo.</span><span class="sxs-lookup"><span data-stu-id="75175-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="75175-129">Crie uma entrada de registro **DllSurrogate** no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="75175-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="75175-130">A entrada **DllSurrogate** informa ao tempo de execução com que seu plug-in deve ser criado em uma instância da dll padrão, alternativa, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="75175-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="75175-131">Para obter informações detalhadas sobre como registrar seu plug-in, consulte [chaves e entradas do registro para um repositório online tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="75175-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="75175-132">Você não precisa criar nenhum código de proxy ou stub para seu plug-in.</span><span class="sxs-lookup"><span data-stu-id="75175-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="75175-133">Todo o suporte a marshaling é fornecido pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="75175-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="75175-134">Você pode usar o assistente de plug-in da loja online para criar rapidamente um plug-in que serve como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="75175-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="75175-135">Para obter mais informações, consulte [instalando o assistente de plug-in da loja online](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="75175-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75175-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75175-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75175-137">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="75175-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




