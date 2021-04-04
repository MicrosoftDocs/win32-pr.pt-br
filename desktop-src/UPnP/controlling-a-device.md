---
title: Controlando um dispositivo
description: Depois de descobrir os dispositivos, você pode controlá-los.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822952"
---
# <a name="controlling-a-device"></a><span data-ttu-id="1c096-103">Controlando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="1c096-103">Controlling a Device</span></span>

<span data-ttu-id="1c096-104">Depois de descobrir os dispositivos, você pode controlá-los.</span><span class="sxs-lookup"><span data-stu-id="1c096-104">Once you have discovered devices, you can control them.</span></span>

<span data-ttu-id="1c096-105">**Para exibir as propriedades do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="1c096-105">**To view device properties**</span></span>

1.  <span data-ttu-id="1c096-106">Selecione um dispositivo na lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="1c096-106">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="1c096-107">Clique em **Propriedades do dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="1c096-107">Click **Device Properties**.</span></span> <span data-ttu-id="1c096-108">A janela **Propriedades do dispositivo** é exibida com as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="1c096-108">The **Device Properties** window appears with the requested information.</span></span>

> [!Note]  
> <span data-ttu-id="1c096-109">A funcionalidade **Exibir apresentação** não está disponível no código de exemplo C++.</span><span class="sxs-lookup"><span data-stu-id="1c096-109">The **View Presentation** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="1c096-110">**Para exibir a página de apresentação de um dispositivo**</span><span class="sxs-lookup"><span data-stu-id="1c096-110">**To view a device's presentation page**</span></span>

1.  <span data-ttu-id="1c096-111">Selecione um dispositivo na lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="1c096-111">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="1c096-112">Clique em **Exibir apresentação**.</span><span class="sxs-lookup"><span data-stu-id="1c096-112">Click **View Presentation**.</span></span> <span data-ttu-id="1c096-113">Uma janela do Internet Explorer é exibida com a página de apresentação solicitada.</span><span class="sxs-lookup"><span data-stu-id="1c096-113">An Internet Explorer window appears with the requested presentation page.</span></span>

> [!Note]  
> <span data-ttu-id="1c096-114">A funcionalidade do **serviço de exibição desc.** não está disponível no código de exemplo de C++.</span><span class="sxs-lookup"><span data-stu-id="1c096-114">The **View Service Desc.** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="1c096-115">**Para exibir uma descrição de serviço**</span><span class="sxs-lookup"><span data-stu-id="1c096-115">**To view a service description**</span></span>

1.  <span data-ttu-id="1c096-116">Você pode inserir a URL para a descrição do serviço no **serviço desc.** Campo de URL.</span><span class="sxs-lookup"><span data-stu-id="1c096-116">You can enter the URL to the service description in the **Service Desc. URL** field.</span></span>

    ![URL de descrição de serviço](images/ucp-url.png)

2.  <span data-ttu-id="1c096-118">Clique em **Exibir serviço desc.** A janela do **Visualizador de descrição de serviço** é exibida.</span><span class="sxs-lookup"><span data-stu-id="1c096-118">Click **View Service Desc.** The **Service Description Viewer** window is displayed.</span></span> <span data-ttu-id="1c096-119">Em seguida, você pode procurar a descrição do serviço usando o modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="1c096-119">You can then browse the service description using the tree view.</span></span> <span data-ttu-id="1c096-120">Essa funcionalidade não está disponível no código de exemplo do C++.</span><span class="sxs-lookup"><span data-stu-id="1c096-120">This functionality is not available in the C++ sample code.</span></span>

    ![janela do Visualizador de descrição de serviço](images/ucp-serv.png)

    <span data-ttu-id="1c096-122">Há cinco comandos que podem ser usados na janela do Visualizador de descrição de serviço.</span><span class="sxs-lookup"><span data-stu-id="1c096-122">There are five commands you can use in the Service Description Viewer window.</span></span>



| <span data-ttu-id="1c096-123">Botão</span><span class="sxs-lookup"><span data-stu-id="1c096-123">Button</span></span>                 | <span data-ttu-id="1c096-124">Ação executada</span><span class="sxs-lookup"><span data-stu-id="1c096-124">Action Performed</span></span>                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c096-125">Go</span><span class="sxs-lookup"><span data-stu-id="1c096-125">Go</span></span>                     | <span data-ttu-id="1c096-126">Carrega o arquivo mostrado no **serviço desc.** Campo de URL.</span><span class="sxs-lookup"><span data-stu-id="1c096-126">Loads the file shown in the **Service Desc. URL** field.</span></span>                                                                                                                              |
| <span data-ttu-id="1c096-127">Definir ação</span><span class="sxs-lookup"><span data-stu-id="1c096-127">Set Action</span></span>             | <span data-ttu-id="1c096-128">Selecione um nome de ação na árvore de descrição de serviço e clique em **definir ação**.</span><span class="sxs-lookup"><span data-stu-id="1c096-128">Select an action name in the service description tree and click **Set Action**.</span></span> <span data-ttu-id="1c096-129">O nome da ação é inserido no campo **ação de invocação** da janela principal do **UCP genérico** .</span><span class="sxs-lookup"><span data-stu-id="1c096-129">The action name is entered into the **Invoke Action** field of the main **Generic UCP** window.</span></span>       |
| <span data-ttu-id="1c096-130">Definir variável</span><span class="sxs-lookup"><span data-stu-id="1c096-130">Set Variable</span></span>           | <span data-ttu-id="1c096-131">Selecione um nome de variável na árvore de descrição de serviço e clique em **definir variável**.</span><span class="sxs-lookup"><span data-stu-id="1c096-131">Select a variable name in the service description tree and click **Set Variable**.</span></span> <span data-ttu-id="1c096-132">O nome da variável é inserido no campo **variável de consulta** da janela principal do **UCP genérico** .</span><span class="sxs-lookup"><span data-stu-id="1c096-132">The variable name is entered into the **Query Variable** field of the main **Generic UCP** window.</span></span> |
| <span data-ttu-id="1c096-133">Preencher lista de variáveis</span><span class="sxs-lookup"><span data-stu-id="1c096-133">Populate Variable List</span></span> | <span data-ttu-id="1c096-134">Carrega todos os nomes de variáveis do serviço na lista de **variáveis de consulta** da janela principal do **UCP genérico** .</span><span class="sxs-lookup"><span data-stu-id="1c096-134">Loads all the service's variable names into the **Query Variable** list of the main **Generic UCP** window.</span></span>                                                                           |
| <span data-ttu-id="1c096-135">Popular lista de ações</span><span class="sxs-lookup"><span data-stu-id="1c096-135">Populate Action List</span></span>   | <span data-ttu-id="1c096-136">Carrega todos os nomes de ação do serviço na lista de **ações de invocação** da janela principal do **UCP genérico** .</span><span class="sxs-lookup"><span data-stu-id="1c096-136">Loads all the service's action names into the **Invoke Action** list of the main **Generic UCP** window.</span></span>                                                                              |



 

<span data-ttu-id="1c096-137">**Para controlar um dispositivo**</span><span class="sxs-lookup"><span data-stu-id="1c096-137">**To control a device**</span></span>

1.  <span data-ttu-id="1c096-138">Na lista **dispositivos encontrados** , selecione o dispositivo que você deseja controlar.</span><span class="sxs-lookup"><span data-stu-id="1c096-138">From the **Devices Found** list, select the device you want to control.</span></span>
2.  <span data-ttu-id="1c096-139">Na lista **escolher serviço** , selecione o serviço que você deseja invocar ou a variável de estado que você deseja consultar.</span><span class="sxs-lookup"><span data-stu-id="1c096-139">From the **Choose Service** list, select the service you want to invoke or state variable you want to query.</span></span>

    ![janela de dispositivos de controle](images/ucp-contr.png)

    > [!Note]  
    > <span data-ttu-id="1c096-141">O conteúdo da **lista de serviços** se baseia no dispositivo selecionado na lista **dispositivos encontrados** .</span><span class="sxs-lookup"><span data-stu-id="1c096-141">The contents of the **Service List** is based on the device selected in the **Devices Found** list.</span></span>

     

3.  <span data-ttu-id="1c096-142">Se você quiser descobrir o valor de uma variável de estado para o serviço selecionado, insira o nome da variável no campo **variável de consulta** para serviço.</span><span class="sxs-lookup"><span data-stu-id="1c096-142">If you want to find out the value of a state variable for the selected service, enter the variable name in the **Query Variable** field for service.</span></span> <span data-ttu-id="1c096-143">Clique em **Consulta**.</span><span class="sxs-lookup"><span data-stu-id="1c096-143">Click **Query**.</span></span> <span data-ttu-id="1c096-144">Os resultados são mostrados no campo **valor do estado da consulta/argumentos fora da ação** .</span><span class="sxs-lookup"><span data-stu-id="1c096-144">The results are shown in the **Query State Value/Action Out Arguments** field.</span></span>
4.  <span data-ttu-id="1c096-145">Se você quiser invocar uma ação para um serviço, insira o nome da ação no campo **ação de invocação** e todos os argumentos no campo **argumentos da ação** .</span><span class="sxs-lookup"><span data-stu-id="1c096-145">If you want to invoke an action for a service, enter the action name in the **Invoke Action** field, and any arguments in the **Action Arguments** field.</span></span> <span data-ttu-id="1c096-146">Clique em **invocar**.</span><span class="sxs-lookup"><span data-stu-id="1c096-146">Click **Invoke**.</span></span> <span data-ttu-id="1c096-147">Os resultados são mostrados no campo **valor do estado da consulta/argumentos fora da ação** , se houver.</span><span class="sxs-lookup"><span data-stu-id="1c096-147">The results are shown in the **Query State Value/Action Out Arguments** field, if any.</span></span>

    <span data-ttu-id="1c096-148">O valor de retorno, se houver, está contido no primeiro argumento out.</span><span class="sxs-lookup"><span data-stu-id="1c096-148">The return value, if any, is contained in the first out argument.</span></span>

    > [!Note]  
    > <span data-ttu-id="1c096-149">Se houver vários argumentos para uma ação, separe-os com espaços.</span><span class="sxs-lookup"><span data-stu-id="1c096-149">If there are multiple arguments for an action, separate them with spaces.</span></span>

     

5.  <span data-ttu-id="1c096-150">Exiba informações de eventos no campo **eventos** para o serviço selecionado.</span><span class="sxs-lookup"><span data-stu-id="1c096-150">View eventing information in the **Events** field for the selected service.</span></span>

 

 




