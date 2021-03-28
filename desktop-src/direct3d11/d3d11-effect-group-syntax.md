---
title: Sintaxe do grupo de efeitos (Direct3D 11)
description: Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104453797"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="f9b69-103">Sintaxe do grupo de efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f9b69-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="f9b69-104">Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="f9b69-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="f9b69-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9b69-105">Parameters</span></span>



| <span data-ttu-id="f9b69-106">Item</span><span class="sxs-lookup"><span data-stu-id="f9b69-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="f9b69-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9b69-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b69-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="f9b69-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="f9b69-109">palavra-chave ecessário.</span><span class="sxs-lookup"><span data-stu-id="f9b69-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="f9b69-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="f9b69-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="f9b69-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f9b69-111">Required.</span></span> <span data-ttu-id="f9b69-112">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome do grupo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="f9b69-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="f9b69-113">Ao contrário das técnicas, os grupos devem ter nomes para garantir que as técnicas tenham um identificador exclusivo (consulte a seção grupos e técnicas abaixo).</span><span class="sxs-lookup"><span data-stu-id="f9b69-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="f9b69-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < anotações ></span><span class="sxs-lookup"><span data-stu-id="f9b69-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="f9b69-115">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="f9b69-115">\[in\] Optional.</span></span> <span data-ttu-id="f9b69-116">Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="f9b69-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="f9b69-117">Para obter a sintaxe, consulte Sintaxe de anotação (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="f9b69-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="f9b69-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="f9b69-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="f9b69-119">"Technique10" ou "technique11".</span><span class="sxs-lookup"><span data-stu-id="f9b69-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="f9b69-120">As técnicas que usam a funcionalidade nova para o Direct3D 11 (5 \_ 0 shaders, BindInterfaces, etc.) devem usar "technique11".</span><span class="sxs-lookup"><span data-stu-id="f9b69-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="f9b69-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Técnicaname</span><span class="sxs-lookup"><span data-stu-id="f9b69-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="f9b69-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f9b69-122">Optional.</span></span> <span data-ttu-id="f9b69-123">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.</span><span class="sxs-lookup"><span data-stu-id="f9b69-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="f9b69-124">Grupos e técnicas</span><span class="sxs-lookup"><span data-stu-id="f9b69-124">Groups and Techniques</span></span>

<span data-ttu-id="f9b69-125">Para manter a compatibilidade com efeitos FX \_ 4 \_ 0, os grupos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f9b69-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="f9b69-126">Há um grupo com nome nulo implícito em torno de todas as técnicas globais.</span><span class="sxs-lookup"><span data-stu-id="f9b69-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="f9b69-127">Considere o seguinte exemplo:</span><span class="sxs-lookup"><span data-stu-id="f9b69-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="f9b69-128">Em C++, é possível obter uma técnica por nome de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="f9b69-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="f9b69-129">Os seguintes comandos encontrarão as técnicas óbvias:</span><span class="sxs-lookup"><span data-stu-id="f9b69-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="f9b69-130">Para garantir que [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funcione da mesma forma que os efeitos 10, todos os grupos definidos devem ter um nome.</span><span class="sxs-lookup"><span data-stu-id="f9b69-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9b69-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9b69-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9b69-132">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="f9b69-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="f9b69-133">Sintaxe da técnica de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f9b69-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





