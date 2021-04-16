---
description: Localizando partições durante a ativação
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Localizando partições durante a ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104571318"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="75cff-103">Localizando partições durante a ativação</span><span class="sxs-lookup"><span data-stu-id="75cff-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="75cff-104">Localizar a partição correta na qual ativar um componente depende do seguinte:</span><span class="sxs-lookup"><span data-stu-id="75cff-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="75cff-105">A chamada de função e os parâmetros usados no programa de chamada para ativar o componente</span><span class="sxs-lookup"><span data-stu-id="75cff-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="75cff-106">Se o componente que está sendo ativado é local ou remoto</span><span class="sxs-lookup"><span data-stu-id="75cff-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="75cff-107">O uso interno do cache de partição</span><span class="sxs-lookup"><span data-stu-id="75cff-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="75cff-108">O programa de chamada</span><span class="sxs-lookup"><span data-stu-id="75cff-108">The Calling Program</span></span>

<span data-ttu-id="75cff-109">COM+ seleciona a partição para a ativação do componente com base em como o programa de chamada ativa o componente.</span><span class="sxs-lookup"><span data-stu-id="75cff-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="75cff-110">Há três ações diferentes que o COM+ pode tomar ao selecionar uma partição para a ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="75cff-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="75cff-111">A ação executada depende de como o programa de chamada instancia o objeto ou seja, se a chamada de função inclui um moniker de partição, que consiste em uma ID de partição e um CLSID, ou inclui apenas um CLSID.</span><span class="sxs-lookup"><span data-stu-id="75cff-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="75cff-112">A tabela a seguir mostra as várias ações que o COM+ pode executar, em ordem de precedência, para localizar uma partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="75cff-113">Chamada de função</span><span class="sxs-lookup"><span data-stu-id="75cff-113">Function call</span></span>                                                  | <span data-ttu-id="75cff-114">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="75cff-114">Parameter</span></span>                                                      | <span data-ttu-id="75cff-115">Ação COM+</span><span class="sxs-lookup"><span data-stu-id="75cff-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75cff-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) ou **GetObject**</span><span class="sxs-lookup"><span data-stu-id="75cff-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="75cff-117">Moniker de partição (inclui ID de partição e CLSID)</span><span class="sxs-lookup"><span data-stu-id="75cff-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="75cff-118">Usa a ID de partição especificada no moniker da partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="75cff-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="75cff-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="75cff-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="75cff-120">CLSID</span></span><br/>                                               | <span data-ttu-id="75cff-121">Usa a ID de partição da partição padrão da identidade do usuário ou a ID da partição que foi adicionada ao contexto durante uma ativação de componente anterior no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="75cff-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="75cff-122">As ações COM+ listadas na tabela anterior são explicadas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="75cff-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="75cff-123">Uso de monikers de partição</span><span class="sxs-lookup"><span data-stu-id="75cff-123">Use of Partition Monikers</span></span>

<span data-ttu-id="75cff-124">Uma partição pode ser selecionada explicitamente dentro de uma chamada de função usando um *moniker de partição*.</span><span class="sxs-lookup"><span data-stu-id="75cff-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="75cff-125">Um moniker de partição é usado dentro do código para especificar explicitamente a partição do componente ativado.</span><span class="sxs-lookup"><span data-stu-id="75cff-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="75cff-126">Se um moniker de partição for usado para localizar a partição, a ativação ocorrerá dessa partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="75cff-127">Ou seja, a ID da partição incluída no moniker tem precedência sobre a partição padrão do usuário ou sobre uma ID de partição que existe no contexto do chamador.</span><span class="sxs-lookup"><span data-stu-id="75cff-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="75cff-128">No código C++, a sintaxe para o uso de um moniker de partição é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="75cff-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="75cff-129">O exemplo a seguir mostra um trecho de código C++, no qual um moniker de partição está sendo usado como um argumento para a função [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :</span><span class="sxs-lookup"><span data-stu-id="75cff-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="75cff-130">No código Visual Basic, a sintaxe de um moniker de partição é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="75cff-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="75cff-131">O exemplo a seguir mostra um trecho de código de Visual Basic, no qual um moniker de partição está sendo usado como um argumento para a função **GetObject** :</span><span class="sxs-lookup"><span data-stu-id="75cff-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="75cff-132">Uso do mapeamento padrão</span><span class="sxs-lookup"><span data-stu-id="75cff-132">Use of Default Mapping</span></span>

<span data-ttu-id="75cff-133">Quando a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) é usada para ativar um componente, usando o CLSID do componente, o com+ usa o mapeamento de identidade de usuário padrão, que é, o conjunto de partições ao qual o usuário está mapeado dentro Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75cff-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="75cff-134">No entanto, se o usuário não estiver mapeado para um conjunto de partições dentro do Active Directory, a partição global será selecionada.</span><span class="sxs-lookup"><span data-stu-id="75cff-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="75cff-135">Uso de IDs de partição e contexto de objeto</span><span class="sxs-lookup"><span data-stu-id="75cff-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="75cff-136">Uma das cinco propriedades atribuídas a uma nova partição é a ID da partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="75cff-137">Quando o programa cliente chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância de um objeto, a ID da partição é adicionada ao contexto.</span><span class="sxs-lookup"><span data-stu-id="75cff-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="75cff-138">O uso da ID de partição do contexto para localizar a partição é importante porque garante que, depois que uma cadeia de ativações for iniciada, a ID da partição permanecerá a mesma, a menos que seja alterada explicitamente por meio de um moniker de partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="75cff-139">Para obter informações adicionais sobre como localizar partições durante a ativação, consulte [componentes e partições em fila do com+](com--queued-components-and-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="75cff-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="75cff-140">Ativação local e remota</span><span class="sxs-lookup"><span data-stu-id="75cff-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="75cff-141">Se o componente que está sendo chamado existir em outro computador, as propriedades da partição (incluindo a ID da partição) serão empacotadas para o outro computador e o componente será ativado da partição empacotada.</span><span class="sxs-lookup"><span data-stu-id="75cff-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="75cff-142">Se nenhuma ID de partição tiver sido empacotada, COM+ usará o conjunto de partições padrão mapeado para a identidade do usuário dentro do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75cff-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="75cff-143">O cache de partição</span><span class="sxs-lookup"><span data-stu-id="75cff-143">The Partition Cache</span></span>

<span data-ttu-id="75cff-144">Em um ambiente de domínio, o COM+ usa os mapeamentos no Active Directory para localizar a partição correta para a ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="75cff-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="75cff-145">No entanto, pesquisas frequentes no Active Directory podem resultar em excesso de tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="75cff-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="75cff-146">Para minimizar o tráfego de rede resultante de pesquisas frequentes de mapeamento de conjunto de usuário para partição no Active Directory, o COM+ usa um *cache de partição*.</span><span class="sxs-lookup"><span data-stu-id="75cff-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="75cff-147">O cache de partição contém os mapeamentos que foram feitos em Active Directory entre as identidades de usuário ou as UOs e seus conjuntos de partições.</span><span class="sxs-lookup"><span data-stu-id="75cff-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="75cff-148">Esse cache de partição está localizado no servidor de aplicativos no qual residem os aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="75cff-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="75cff-149">Quando o COM+ precisa determinar a partição padrão de um usuário ou validar os direitos de acesso de um usuário para uma partição, ele verifica o cache de partição localmente para procurar o mapeamento do usuário, em vez de verificar Active Directory remotamente.</span><span class="sxs-lookup"><span data-stu-id="75cff-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="75cff-150">Se a pesquisa no cache da partição falhar, o COM+ verificará Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75cff-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="75cff-151">Se a pesquisa for bem-sucedida no Active Directory, o COM+ armazenará o mapeamento no cache da partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="75cff-152">Na próxima vez em que uma pesquisa for feita para esse mapeamento de usuário para partição, o COM+ a encontrará no cache de partição.</span><span class="sxs-lookup"><span data-stu-id="75cff-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="75cff-153">A ilustração a seguir mostra o processo que o COM+ usa para localizar uma partição para a ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="75cff-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![Diagrama que mostra uma árvore de solução de problemas para o processo que o COM+ usa para localizar uma partição para a ativação do componente.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="75cff-155">O tamanho do cache e o tempo de expiração das entradas de cache são definidos por meio de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="75cff-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="75cff-156">Para obter informações sobre como configurar essas chaves do registro, consulte [criando e configurando partições com+](creating-and-configuring-com--partitions.md).</span><span class="sxs-lookup"><span data-stu-id="75cff-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="75cff-157">Se um computador servidor estiver desconectado da rede e o mapeamento de usuário para partição for alterado enquanto o servidor estiver desconectado, o cache de partição poderá conter mapeamento de usuário para partição desatualizado.</span><span class="sxs-lookup"><span data-stu-id="75cff-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="75cff-158">Isso pode resultar em um erro de ativação se o mapeamento de usuário para partição for o mecanismo usado para ativar um componente.</span><span class="sxs-lookup"><span data-stu-id="75cff-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75cff-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75cff-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75cff-160">Localizando um componente para ativação</span><span class="sxs-lookup"><span data-stu-id="75cff-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

