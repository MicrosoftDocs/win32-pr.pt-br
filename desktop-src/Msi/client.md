---
description: O objeto cliente representa uma relação entre um componente e um produto cliente.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objeto de cliente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780523"
---
# <a name="client-object"></a><span data-ttu-id="3ba21-103">Objeto de cliente</span><span class="sxs-lookup"><span data-stu-id="3ba21-103">Client object</span></span>

<span data-ttu-id="3ba21-104">O objeto cliente representa uma relação entre um componente e um produto cliente.</span><span class="sxs-lookup"><span data-stu-id="3ba21-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="3ba21-105">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="3ba21-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="3ba21-106">Esse objeto está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="3ba21-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="3ba21-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3ba21-107">Members</span></span>

<span data-ttu-id="3ba21-108">O objeto de **cliente** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ba21-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="3ba21-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ba21-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ba21-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ba21-110">Properties</span></span>

<span data-ttu-id="3ba21-111">O objeto de **cliente** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ba21-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="3ba21-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3ba21-112">Property</span></span>                                                 | <span data-ttu-id="3ba21-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ba21-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="3ba21-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="3ba21-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="3ba21-115">O código do componente em questão.</span><span class="sxs-lookup"><span data-stu-id="3ba21-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="3ba21-116">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="3ba21-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="3ba21-117">O contexto do produto.</span><span class="sxs-lookup"><span data-stu-id="3ba21-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="3ba21-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="3ba21-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="3ba21-119">O produto cliente do componente em questão.</span><span class="sxs-lookup"><span data-stu-id="3ba21-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="3ba21-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="3ba21-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="3ba21-121">O SID do usuário para o componente.</span><span class="sxs-lookup"><span data-stu-id="3ba21-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="3ba21-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba21-122">Requirements</span></span>



| <span data-ttu-id="3ba21-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba21-123">Requirement</span></span> | <span data-ttu-id="3ba21-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba21-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba21-125">Versão</span><span class="sxs-lookup"><span data-stu-id="3ba21-125">Version</span></span><br/> | <span data-ttu-id="3ba21-126">Windows Installer 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3ba21-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="3ba21-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba21-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="3ba21-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ba21-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ba21-129">IID</span><span class="sxs-lookup"><span data-stu-id="3ba21-129">IID</span></span><br/>     | <span data-ttu-id="3ba21-130">IID \_ IClient é definido como 000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3ba21-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3ba21-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba21-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba21-132">Usando a interface de automação</span><span class="sxs-lookup"><span data-stu-id="3ba21-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="3ba21-133">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3ba21-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




