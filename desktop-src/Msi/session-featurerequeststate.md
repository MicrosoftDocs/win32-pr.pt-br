---
description: A propriedade FeatureRequestState é uma propriedade de leitura/gravação do objeto de sessão.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propriedade Session. FeatureRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766385"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="01442-103">Propriedade Session. FeatureRequestState</span><span class="sxs-lookup"><span data-stu-id="01442-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="01442-104">A propriedade **FeatureRequestState** é uma propriedade de leitura/gravação do objeto de [**sessão**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="01442-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="01442-105">Ele pode ser usado para obter o estado de ação atual de um recurso ou para solicitar uma alteração na ação de um recurso e seus sub-recursos.</span><span class="sxs-lookup"><span data-stu-id="01442-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="01442-106">O recurso deve ser nomeado na tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="01442-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="01442-107">Se uma alteração no estado de ação de um recurso for solicitada, o estado de ação de todos os componentes do recurso alterado também poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="01442-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="01442-108">O estado de ação dos componentes compartilhados por mais de um recurso será alterado conforme apropriado com base no novo estado de ação do recurso (consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="01442-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="01442-109">A propriedade **FeatureRequestState** também pode ser usada para configurar todos os recursos de uma vez, especificando a palavra-chave All em vez de um nome de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="01442-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="01442-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="01442-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01442-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="01442-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="01442-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="01442-112">Property value</span></span>

<span data-ttu-id="01442-113">Cadeia de caracteres necessária que especifica o nome do recurso a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="01442-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="01442-114">Para definir todos os recursos para um estado de solicitação desejado, use a palavra reservada não diferencia maiúsculas de minúsculas: ALL.</span><span class="sxs-lookup"><span data-stu-id="01442-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="01442-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="01442-115">Remarks</span></span>

<span data-ttu-id="01442-116">O método [**SetInstallLevel**](session-setinstalllevel.md) deve ser chamado antes de chamar **FeatureRequestState**.</span><span class="sxs-lookup"><span data-stu-id="01442-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="01442-117">Se o estado atual do recurso estiver sendo solicitado, a propriedade **FeatureRequestState** retornará um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="01442-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="01442-118">Nome do estado de seleção</span><span class="sxs-lookup"><span data-stu-id="01442-118">Selection state name</span></span>         | <span data-ttu-id="01442-119">Significado</span><span class="sxs-lookup"><span data-stu-id="01442-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="01442-120">msiInstallStateUnknown =-1</span><span class="sxs-lookup"><span data-stu-id="01442-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="01442-121">Nenhuma ação é tomada para o recurso.</span><span class="sxs-lookup"><span data-stu-id="01442-121">No action is taken for the feature.</span></span> <span data-ttu-id="01442-122">Isso é equivalente a NULL.</span><span class="sxs-lookup"><span data-stu-id="01442-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="01442-123">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="01442-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="01442-124">O recurso deve ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="01442-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="01442-125">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="01442-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="01442-126">O recurso deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="01442-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="01442-127">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="01442-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="01442-128">O recurso deve ser instalado como o local de execução.</span><span class="sxs-lookup"><span data-stu-id="01442-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="01442-129">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="01442-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="01442-130">O recurso deve ser instalado como execução de origem.</span><span class="sxs-lookup"><span data-stu-id="01442-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="01442-131">msiInstallStateDefault = 5</span><span class="sxs-lookup"><span data-stu-id="01442-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="01442-132">O recurso deve ser reinstalado com o estado de ação atual do recurso.</span><span class="sxs-lookup"><span data-stu-id="01442-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="01442-133">Por exemplo, o seguinte Obtém o estado atual de "MyFeature" de uma ação personalizada do VBScript.</span><span class="sxs-lookup"><span data-stu-id="01442-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="01442-134">Se o estado do recurso estiver sendo configurado, a propriedade **FeatureRequestState** deverá ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="01442-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="01442-135">Nome do estado de seleção</span><span class="sxs-lookup"><span data-stu-id="01442-135">Selection state name</span></span>          | <span data-ttu-id="01442-136">Significado</span><span class="sxs-lookup"><span data-stu-id="01442-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="01442-137">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="01442-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="01442-138">Anuncie o recurso.</span><span class="sxs-lookup"><span data-stu-id="01442-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="01442-139">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="01442-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="01442-140">Remova o recurso.</span><span class="sxs-lookup"><span data-stu-id="01442-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="01442-141">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="01442-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="01442-142">Instale o recurso como Run-local.</span><span class="sxs-lookup"><span data-stu-id="01442-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="01442-143">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="01442-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="01442-144">Instale o recurso como execução de origem.</span><span class="sxs-lookup"><span data-stu-id="01442-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="01442-145">Por exemplo, as seguintes solicitações de uma ação personalizada do VBScript que "MyFeature" serão instaladas para serem executadas localmente no computador.</span><span class="sxs-lookup"><span data-stu-id="01442-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="01442-146">Quando **FeatureRequestState** é chamado, o instalador tenta definir o estado de ação de cada componente vinculado ao recurso especificado para o estado especificado, o melhor possível.</span><span class="sxs-lookup"><span data-stu-id="01442-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="01442-147">No entanto, há situações comuns em que a solicitação não pode ser totalmente respeitada.</span><span class="sxs-lookup"><span data-stu-id="01442-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="01442-148">Por exemplo, se um recurso estiver vinculado a dois componentes, componente A e componente B, por meio da tabela [FeatureComponents](featurecomponents-table.md) e o componente a tem o atributo **msidbComponentAttributesLocalOnly** e o componente b tem o atributo **msidbComponentAttributesSourceOnly** .</span><span class="sxs-lookup"><span data-stu-id="01442-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="01442-149">Nesse caso, se **FeatureRequestState** for chamado com um estado solicitado de MsiInstallStateLocal ou msiInstallStateSource, a solicitação não poderá ser respeitada para ambos os componentes.</span><span class="sxs-lookup"><span data-stu-id="01442-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="01442-150">Nesse caso, ambos os componentes podem ser ativados com o componente A definido como msiInstallStateLocal e o componente B definido como msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="01442-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="01442-151">Se mais de um recurso estiver vinculado a um único componente, o estado de ação final desse componente será determinado da seguinte maneira: se pelo menos um recurso chamar o componente a ser instalado localmente, ele será instalado msiInstallStateLocal.</span><span class="sxs-lookup"><span data-stu-id="01442-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="01442-152">Se pelo menos um recurso chamar o componente a ser executado da mídia de origem, ele será instalado msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="01442-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="01442-153">Se pelo menos um recurso chamar para a remoção do componente, o estado de ação será msiInstallStateAbsent.</span><span class="sxs-lookup"><span data-stu-id="01442-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="01442-154">Para obter mais informações sobre como os recursos são selecionados para instalação, consulte a tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="01442-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="01442-155">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="01442-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01442-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01442-156">Requirements</span></span>



| <span data-ttu-id="01442-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="01442-157">Requirement</span></span> | <span data-ttu-id="01442-158">Valor</span><span class="sxs-lookup"><span data-stu-id="01442-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01442-159">Versão</span><span class="sxs-lookup"><span data-stu-id="01442-159">Version</span></span><br/> | <span data-ttu-id="01442-160">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="01442-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="01442-161">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01442-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="01442-162">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="01442-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="01442-163">DLL</span><span class="sxs-lookup"><span data-stu-id="01442-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="01442-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01442-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="01442-165">IID</span><span class="sxs-lookup"><span data-stu-id="01442-165">IID</span></span><br/>     | <span data-ttu-id="01442-166">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="01442-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="01442-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="01442-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01442-168">**Session**</span><span class="sxs-lookup"><span data-stu-id="01442-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="01442-169">Recurso</span><span class="sxs-lookup"><span data-stu-id="01442-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




