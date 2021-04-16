---
title: InprocServer32
description: Registra um servidor em processo de 32 bits e especifica o modelo de Threading do apartamento no qual o servidor pode ser executado.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- A chave do registro InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498768"
---
# <a name="inprocserver32"></a><span data-ttu-id="e7e57-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="e7e57-104">InprocServer32</span></span>

<span data-ttu-id="e7e57-105">Registra um servidor em processo de 32 bits e especifica o modelo de Threading do apartamento no qual o servidor pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="e7e57-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e7e57-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="e7e57-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="e7e57-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7e57-107">Remarks</span></span>

<span data-ttu-id="e7e57-108">**ThreadingModel** é um valor de **\_ sz de reg** que especifica o modelo de Threading.</span><span class="sxs-lookup"><span data-stu-id="e7e57-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="e7e57-109">Os valores possíveis são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7e57-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="e7e57-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e7e57-110">Value</span></span>     | <span data-ttu-id="e7e57-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7e57-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="e7e57-112">Sta</span><span class="sxs-lookup"><span data-stu-id="e7e57-112">Apartment</span></span> | <span data-ttu-id="e7e57-113">Apartamento de thread único</span><span class="sxs-lookup"><span data-stu-id="e7e57-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="e7e57-114">Ambos</span><span class="sxs-lookup"><span data-stu-id="e7e57-114">Both</span></span>      | <span data-ttu-id="e7e57-115">Apartamento de thread único ou multithread</span><span class="sxs-lookup"><span data-stu-id="e7e57-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="e7e57-116">Gratuita</span><span class="sxs-lookup"><span data-stu-id="e7e57-116">Free</span></span>      | <span data-ttu-id="e7e57-117">Apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="e7e57-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="e7e57-118">Neutro</span><span class="sxs-lookup"><span data-stu-id="e7e57-118">Neutral</span></span>   | <span data-ttu-id="e7e57-119">Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="e7e57-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="e7e57-120">Você deve usar o mesmo valor para cada objeto fornecido pelo servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="e7e57-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="e7e57-121">Se **ThreadingModel** não estiver presente ou não estiver definido como um valor, o servidor será carregado no primeiro apartamento que foi inicializado no processo.</span><span class="sxs-lookup"><span data-stu-id="e7e57-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="e7e57-122">Esse apartamento às vezes é chamado de STA (single-threaded apartment).</span><span class="sxs-lookup"><span data-stu-id="e7e57-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="e7e57-123">Se o primeiro STA em um processo for inicializado por COM, em vez de uma chamada explícita para o [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), ele será chamado de Sta do host.</span><span class="sxs-lookup"><span data-stu-id="e7e57-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="e7e57-124">Por exemplo, COM cria um host STA se um servidor em processo a ser carregado requer um STA, mas atualmente não há um STA no processo.</span><span class="sxs-lookup"><span data-stu-id="e7e57-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="e7e57-125">Sempre que possível, o servidor em processo é carregado no mesmo apartamento que o cliente que o carrega.</span><span class="sxs-lookup"><span data-stu-id="e7e57-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="e7e57-126">Se o modelo de Threading do apartamento do cliente não for compatível com o modelo especificado, o servidor será carregado conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7e57-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="e7e57-127">Modelo de Threading do servidor</span><span class="sxs-lookup"><span data-stu-id="e7e57-127">Threading model of server</span></span> | <span data-ttu-id="e7e57-128">O servidor de apartamento é executado em</span><span class="sxs-lookup"><span data-stu-id="e7e57-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="e7e57-129">STA principal</span><span class="sxs-lookup"><span data-stu-id="e7e57-129">Main STA</span></span>                   |
| <span data-ttu-id="e7e57-130">Ambos</span><span class="sxs-lookup"><span data-stu-id="e7e57-130">Both</span></span>                      | <span data-ttu-id="e7e57-131">Mesmo apartamento como cliente</span><span class="sxs-lookup"><span data-stu-id="e7e57-131">Same apartment as client</span></span>   |
| <span data-ttu-id="e7e57-132">Gratuita</span><span class="sxs-lookup"><span data-stu-id="e7e57-132">Free</span></span>                      | <span data-ttu-id="e7e57-133">Apartamento multithread</span><span class="sxs-lookup"><span data-stu-id="e7e57-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="e7e57-134">Neutro</span><span class="sxs-lookup"><span data-stu-id="e7e57-134">Neutral</span></span>                   | <span data-ttu-id="e7e57-135">Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="e7e57-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="e7e57-136">Se o modelo de Threading do servidor for Apartment, o apartamento no qual o servidor é carregado dependerá do apartamento em que o cliente está sendo executado, conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7e57-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="e7e57-137">O cliente de apartamento é executado em</span><span class="sxs-lookup"><span data-stu-id="e7e57-137">Apartment client is run in</span></span> | <span data-ttu-id="e7e57-138">O servidor de apartamento é executado em</span><span class="sxs-lookup"><span data-stu-id="e7e57-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="e7e57-139">Multithread</span><span class="sxs-lookup"><span data-stu-id="e7e57-139">Multithreaded</span></span>              | <span data-ttu-id="e7e57-140">Host STA</span><span class="sxs-lookup"><span data-stu-id="e7e57-140">Host STA</span></span>                   |
| <span data-ttu-id="e7e57-141">Neutro (no thread STA)</span><span class="sxs-lookup"><span data-stu-id="e7e57-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="e7e57-142">Mesmo apartamento como cliente</span><span class="sxs-lookup"><span data-stu-id="e7e57-142">Same apartment as client</span></span>   |
| <span data-ttu-id="e7e57-143">Neutro (no thread MTA)</span><span class="sxs-lookup"><span data-stu-id="e7e57-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="e7e57-144">Host STA</span><span class="sxs-lookup"><span data-stu-id="e7e57-144">Host STA</span></span>                   |



 

<span data-ttu-id="e7e57-145">COM também pode criar um MTA (multithreaded apartment) do host.</span><span class="sxs-lookup"><span data-stu-id="e7e57-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="e7e57-146">Se um cliente em um apartamento de thread único solicitar um servidor em processo cujo modelo de Threading seja gratuito quando não houver MTA no processo, o COM criará um MTA de host e carregará o servidor nele.</span><span class="sxs-lookup"><span data-stu-id="e7e57-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="e7e57-147">Para um servidor em processo de 32 bits, as chaves [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable**](insertable.md) devem ser registradas.</span><span class="sxs-lookup"><span data-stu-id="e7e57-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="e7e57-148">A entrada **InprocServer** é necessária apenas para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e7e57-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="e7e57-149">Se ele estiver ausente, a classe ainda funcionará, mas não poderá ser carregada em aplicativos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e7e57-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="e7e57-150">Se um contêiner estiver pesquisando o registro de um servidor em processo, a versão de 16 bits terá prioridade com um contêiner de 16 bits e a versão de 32 bits terá prioridade com um contêiner de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e7e57-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e57-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7e57-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e57-152">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="e7e57-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




