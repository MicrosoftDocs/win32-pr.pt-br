---
description: O objeto ComponentInfo representa detalhes adicionais sobre um componente que pode ser obtido por meio de uma chamada de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objeto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748781"
---
# <a name="componentinfo-object"></a><span data-ttu-id="61d2a-103">Objeto ComponentInfo</span><span class="sxs-lookup"><span data-stu-id="61d2a-103">ComponentInfo object</span></span>

<span data-ttu-id="61d2a-104">O objeto ComponentInfo representa detalhes adicionais sobre um componente que pode ser obtido por meio de uma chamada de MsiGetComponentPathEx.</span><span class="sxs-lookup"><span data-stu-id="61d2a-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="61d2a-105">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="61d2a-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="61d2a-106">Esse objeto está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="61d2a-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="61d2a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="61d2a-107">Members</span></span>

<span data-ttu-id="61d2a-108">O objeto **ComponentInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61d2a-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="61d2a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61d2a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61d2a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61d2a-110">Properties</span></span>

<span data-ttu-id="61d2a-111">O objeto **ComponentInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61d2a-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="61d2a-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="61d2a-112">Property</span></span>                                                        | <span data-ttu-id="61d2a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="61d2a-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="61d2a-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="61d2a-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="61d2a-115">O código do componente em questão.</span><span class="sxs-lookup"><span data-stu-id="61d2a-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="61d2a-116">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="61d2a-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="61d2a-117">O caminho do componente.</span><span class="sxs-lookup"><span data-stu-id="61d2a-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="61d2a-118">**Status**</span><span class="sxs-lookup"><span data-stu-id="61d2a-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="61d2a-119">O estado do componente.</span><span class="sxs-lookup"><span data-stu-id="61d2a-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="61d2a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61d2a-120">Requirements</span></span>



| <span data-ttu-id="61d2a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61d2a-121">Requirement</span></span> | <span data-ttu-id="61d2a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="61d2a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61d2a-123">Versão</span><span class="sxs-lookup"><span data-stu-id="61d2a-123">Version</span></span><br/> | <span data-ttu-id="61d2a-124">Windows Installer 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="61d2a-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="61d2a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="61d2a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="61d2a-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61d2a-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="61d2a-127">IID</span><span class="sxs-lookup"><span data-stu-id="61d2a-127">IID</span></span><br/>     | <span data-ttu-id="61d2a-128">IID \_ IComponentInfo é definido como 000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="61d2a-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="61d2a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="61d2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d2a-130">Usando a interface de automação</span><span class="sxs-lookup"><span data-stu-id="61d2a-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="61d2a-131">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="61d2a-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




