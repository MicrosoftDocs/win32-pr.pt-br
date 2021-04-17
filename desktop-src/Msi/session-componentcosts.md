---
description: A propriedade ComponentCosts do objeto Session retorna um objeto Recordlist que enumera o espaço em disco por unidade necessário para instalar um componente.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Propriedade Session. ComponentCosts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754346"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="8c1ea-103">Propriedade Session. ComponentCosts</span><span class="sxs-lookup"><span data-stu-id="8c1ea-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="8c1ea-104">A propriedade ComponentCosts do objeto [**Session**](session-object.md) retorna um objeto [**recordlist**](recordlist-object.md) que enumera o espaço em disco por unidade necessário para instalar um componente.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="8c1ea-105">Essas informações são usadas pela interface do usuário para exibir o espaço em disco necessário para todas as unidades.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="8c1ea-106">Os custos de espaço em disco retornados estão em múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="8c1ea-107">A propriedade ComponentCosts deve ser usada somente depois que o instalador concluir o [custo do arquivo](file-costing.md) e após a [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8c1ea-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="8c1ea-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1ea-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c1ea-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="8c1ea-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8c1ea-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="8c1ea-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c1ea-111">Remarks</span></span>

<span data-ttu-id="8c1ea-112">Para obter o custo total, adicione os custos de todos os componentes mais o custo do mecanismo do instalador (componente = "").</span><span class="sxs-lookup"><span data-stu-id="8c1ea-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="8c1ea-113">ComponentCosts retorna um [**objeto recordlist**](recordlist-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c1ea-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="8c1ea-114">Cada registro no objeto Recordlist retornado tem os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="8c1ea-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="8c1ea-115">Campo</span><span class="sxs-lookup"><span data-stu-id="8c1ea-115">Field</span></span> | <span data-ttu-id="8c1ea-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c1ea-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="8c1ea-117">1</span><span class="sxs-lookup"><span data-stu-id="8c1ea-117">1</span></span>     | <span data-ttu-id="8c1ea-118">Nome da unidade/volume</span><span class="sxs-lookup"><span data-stu-id="8c1ea-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="8c1ea-119">2</span><span class="sxs-lookup"><span data-stu-id="8c1ea-119">2</span></span>     | <span data-ttu-id="8c1ea-120">Custo final do espaço em disco em múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="8c1ea-121">3</span><span class="sxs-lookup"><span data-stu-id="8c1ea-121">3</span></span>     | <span data-ttu-id="8c1ea-122">Custo temporário de espaço em disco em múltiplos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8c1ea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c1ea-123">Requirements</span></span>



| <span data-ttu-id="8c1ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c1ea-124">Requirement</span></span> | <span data-ttu-id="8c1ea-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8c1ea-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1ea-126">Versão</span><span class="sxs-lookup"><span data-stu-id="8c1ea-126">Version</span></span><br/> | <span data-ttu-id="8c1ea-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8c1ea-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c1ea-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8c1ea-129">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c1ea-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8c1ea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8c1ea-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c1ea-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c1ea-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8c1ea-132">IID</span><span class="sxs-lookup"><span data-stu-id="8c1ea-132">IID</span></span><br/>     | <span data-ttu-id="8c1ea-133">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8c1ea-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




