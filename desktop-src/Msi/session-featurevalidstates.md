---
description: A propriedade FeatureValidStates do objeto Session retorna um inteiro que representa os sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Propriedade Session. FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751422"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="bbab0-103">Propriedade Session. FeatureValidStates</span><span class="sxs-lookup"><span data-stu-id="bbab0-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="bbab0-104">A propriedade **FeatureValidStates** do objeto [**Session**](session-object.md) retorna um inteiro que representa os sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="bbab0-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="bbab0-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bbab0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbab0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbab0-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="bbab0-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bbab0-107">Property value</span></span>

<span data-ttu-id="bbab0-108">Nome de cadeia de caracteres necessário do item de recurso cujos Estados de instalação válidos devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="bbab0-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbab0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbab0-109">Remarks</span></span>

<span data-ttu-id="bbab0-110">O valor de retorno é composto de sinalizadores de bit da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="bbab0-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="bbab0-111">Bit 0: se definido, local é um estado válido.</span><span class="sxs-lookup"><span data-stu-id="bbab0-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="bbab0-112">Bit 1: se definido, a origem será um estado válido.</span><span class="sxs-lookup"><span data-stu-id="bbab0-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="bbab0-113">A propriedade **FeatureValidStates** só terá sucesso depois que o instalador tiver chamado as ações [CostInitialize](costinitialize-action.md) e [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bbab0-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="bbab0-114">**FeatureValidStates** determina a validade do estado consultando todos os componentes vinculados ao recurso especificado sem levar em conta o estado atual instalado de qualquer componente.</span><span class="sxs-lookup"><span data-stu-id="bbab0-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="bbab0-115">Os Estados válidos possíveis para um recurso são determinados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bbab0-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="bbab0-116">Se o recurso não contiver componentes, a origem INSTALLstate \_ local e InstallState \_ serão Estados válidos para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbab0-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="bbab0-117">Se pelo menos um componente do recurso tiver um atributo de msidbComponentAttributesLocalOnly ou msidbComponentAttributesOptional, INSTALLstate \_ local será um estado válido para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbab0-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="bbab0-118">Se pelo menos um componente do recurso tiver um atributo de msidbComponentAttributesSourceOnly ou msidbComponentAttributesOptional, a origem INSTALLstate \_ será um estado válido para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbab0-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="bbab0-119">Se um arquivo de um componente pertencente ao recurso for corrigido ou de uma fonte compactada, a origem INSTALLstate \_ não será incluída como um estado válido para o recurso.</span><span class="sxs-lookup"><span data-stu-id="bbab0-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="bbab0-120">\_A notificação InstallState não será um estado válido se o recurso não permitir anúncio (msidbFeatureAttributesDisallowAdvertise) ou o recurso exigir o suporte de plataforma para anúncio (msidbFeatureAttributesNoUnsupportedAdvertise) e a plataforma não oferecer suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="bbab0-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="bbab0-121">INSTALLstate \_ ausente é um estado válido para o recurso se seus atributos não incluírem msidbFeatureAttributesUIDisallowAbsent.</span><span class="sxs-lookup"><span data-stu-id="bbab0-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="bbab0-122">Os Estados válidos para recursos filho marcados para seguir o recurso pai (msidbFeatureAttributesFollowParent) são baseados na ação do recurso pai ou no estado instalado.</span><span class="sxs-lookup"><span data-stu-id="bbab0-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="bbab0-123">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="bbab0-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbab0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbab0-124">Requirements</span></span>



| <span data-ttu-id="bbab0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbab0-125">Requirement</span></span> | <span data-ttu-id="bbab0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bbab0-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbab0-127">Versão</span><span class="sxs-lookup"><span data-stu-id="bbab0-127">Version</span></span><br/> | <span data-ttu-id="bbab0-128">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbab0-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbab0-129">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbab0-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbab0-130">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbab0-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bbab0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bbab0-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbab0-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbab0-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bbab0-133">IID</span><span class="sxs-lookup"><span data-stu-id="bbab0-133">IID</span></span><br/>     | <span data-ttu-id="bbab0-134">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bbab0-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




