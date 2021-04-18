---
description: Visão geral do modelo em cascata para a classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: O modelo RealTimeStylus em cascata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564635"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="8c0ca-103">O modelo RealTimeStylus em cascata</span><span class="sxs-lookup"><span data-stu-id="8c0ca-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="8c0ca-104">O modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata permite que você use dois objetos **RealTimeStylus** , cada um executando em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="8c0ca-105">Com esse modelo, você anexa um objeto **RealTimeStylus** secundário a um objeto **RealTimeStylus** primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="8c0ca-106">O objeto **RealTimeStylus** secundário é anexado como o único plug-in assíncrono na coleção de plug-ins assíncrono do objeto **RealTimeStylus** primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="8c0ca-107">O modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata pode ser útil nos cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="8c0ca-108">Você pode adicionar determinadas tarefas que podem ser computacionalmente exigentes, ainda que ainda exijam acesso em tempo real ao fluxo de dados da caneta do Tablet, como reconhecimento de gestos com vários traços, à coleção de plug-ins síncrona do objeto [**RealTimeStylus**](realtimestylus-class.md) secundário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="8c0ca-109">Você pode distribuir a carga computacional de seus plug-ins síncronos em dois threads, reduzindo atrasos na coleta de tintas em alguns Tablet PCs.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="8c0ca-110">O diagrama a seguir ilustra o fluxo de dados da caneta do Tablet por meio de dois objetos [**RealTimeStylus**](realtimestylus-class.md) em cascata e suas coleções de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![ilustração mostrando fluxo de dados RealTimeStylus em cascata](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="8c0ca-112">Neste diagrama, a letra do círculo "A" representa os dados da caneta do Tablet que já foram processados pelos objetos [**RealTimeStylus**](realtimestylus-class.md) primários e secundários e que foram colocados na fila de saída do objeto **RealTimeStylus** secundário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="8c0ca-113">O círculo "B" representa os dados da caneta do Tablet que já foram processados pelo objeto **RealTimeStylus** primário e adicionados à fila de saída do objeto **RealTimeStylus** primário e ainda não foram enviados para o objeto **RealTimeStylus** secundário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="8c0ca-114">O círculo "C" representa os dados da caneta eletrônica que o objeto **RealTimeStylus** primário está processando no momento.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="8c0ca-115">Ele é enviado para a coleção de plug-ins síncrona e colocado na fila de saída.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="8c0ca-116">O círculo vazio representa a posição na fila de saída em que os dados futuros da caneta do Tablet são adicionados.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="8c0ca-117">Restrições</span><span class="sxs-lookup"><span data-stu-id="8c0ca-117">Constraints</span></span>

<span data-ttu-id="8c0ca-118">Se você usar o construtor [**RealTimeStylus**](realtimestylus-class.md) padrão, criará um objeto **RealTimeStylus** que só pode aceitar a entrada de outro objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="8c0ca-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="8c0ca-119">A lista a seguir descreve as restrições associadas ao uso do modelo [**RealTimeStylus**](realtimestylus-class.md) em cascata.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="8c0ca-120">Somente dois objetos [**RealTimeStylus**](realtimestylus-class.md) podem ser usados, um objeto **RealTimeStylus** primário e um objeto **RealTimeStylus** secundário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="8c0ca-121">O objeto [**RealTimeStylus**](realtimestylus-class.md) primário deve ser criado com um construtor que usa o parâmetro **attachedControl** ou *Handle* .</span><span class="sxs-lookup"><span data-stu-id="8c0ca-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="8c0ca-122">O objeto **RealTimeStylus** secundário deve ser criado com o Construtor no-Argument.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="8c0ca-123">O objeto [**RealTimeStylus**](realtimestylus-class.md) secundário deve ser o único plug-in assíncrono na coleção de plug-ins assíncrono do objeto **RealTimeStylus** primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="8c0ca-124">Um objeto [**RealTimeStylus**](realtimestylus-class.md) secundário só pode ser anexado a um objeto **RealTimeStylus** primário por vez.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="8c0ca-125">Se ele for adicionado a um segundo objeto **RealTimeStylus** primário, o método [Add](/previous-versions/ms824814(v=msdn.10)) lançará uma exceção e o objeto **RealTimeStylus** secundário não será anexado ao segundo objeto **RealTimeStylus** primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="8c0ca-126">O comportamento de alguns dos membros do objeto [**RealTimeStylus**](realtimestylus-class.md) secundário é modificado.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="8c0ca-127">A tabela a seguir descreve o comportamento modificado desses membros.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="8c0ca-128">Membro</span><span class="sxs-lookup"><span data-stu-id="8c0ca-128">Member</span></span></th>
    <th><span data-ttu-id="8c0ca-129">Comportamento</span><span class="sxs-lookup"><span data-stu-id="8c0ca-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="8c0ca-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="8c0ca-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="8c0ca-131">Esse método retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="8c0ca-132">Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, esse método retornará o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8c0ca-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="8c0ca-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="8c0ca-134">Esse método gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="8c0ca-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="8c0ca-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="8c0ca-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="8c0ca-136">Esse método retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="8c0ca-137">Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, esse método retornará uma matriz vazia.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="8c0ca-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="8c0ca-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="8c0ca-139">Obter essa propriedade retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="8c0ca-140">Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, obter essa propriedade retornará o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="8c0ca-141">A definição dessa propriedade gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="8c0ca-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="8c0ca-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span><span class="sxs-lookup"><span data-stu-id="8c0ca-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="8c0ca-143">Obter essa propriedade retorna as informações do objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primário.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="8c0ca-144">Se o <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundário não estiver anexado a um objeto <strong>RealTimeStylus</strong> primário, obter essa propriedade retornará o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="8c0ca-145">A definição dessa propriedade gera uma exceção <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="8c0ca-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="8c0ca-146">O objeto [**RealTimeStylus**](realtimestylus-class.md) pai deve parar de funcionar quando o **RealTimeStylus** filho é Descartado.</span><span class="sxs-lookup"><span data-stu-id="8c0ca-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
