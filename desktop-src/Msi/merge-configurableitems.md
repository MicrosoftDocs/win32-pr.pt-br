---
description: A propriedade ConfigurableItems somente leitura do objeto de mesclagem retorna uma coleção ConfigurableItem objetos, cada um representando uma única linha da Tabela ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.ConfigPropriedade urableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759383"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="a2b49-103">Merge.ConfigPropriedade urableItems</span><span class="sxs-lookup"><span data-stu-id="a2b49-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="a2b49-104">A propriedade **ConfigurableItems** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção [**ConfigurableItem**](configurableitem-object.md) objetos, cada um representando uma única linha da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="a2b49-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="a2b49-105">Semanticamente, cada interface no enumerador representa um item que pode ser configurado pelo consumidor do módulo.</span><span class="sxs-lookup"><span data-stu-id="a2b49-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="a2b49-106">A coleção é uma coleção somente leitura e implementa as interfaces de coleção somente leitura padrão de item (), Count () e \_ NewEnum ().</span><span class="sxs-lookup"><span data-stu-id="a2b49-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="a2b49-107">O enumerador **IEnumMsmConfigItems** implementa Next (), ignore (), Reset () e clone () com a semântica padrão.</span><span class="sxs-lookup"><span data-stu-id="a2b49-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="a2b49-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a2b49-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b49-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2b49-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="a2b49-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2b49-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="a2b49-111">C++</span><span class="sxs-lookup"><span data-stu-id="a2b49-111">C++</span></span>

<span data-ttu-id="a2b49-112">Consulte [**obter \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) a função ConfigurableItems.</span><span class="sxs-lookup"><span data-stu-id="a2b49-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b49-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b49-113">Requirements</span></span>



| <span data-ttu-id="a2b49-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b49-114">Requirement</span></span> | <span data-ttu-id="a2b49-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b49-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b49-116">Versão</span><span class="sxs-lookup"><span data-stu-id="a2b49-116">Version</span></span><br/> | <span data-ttu-id="a2b49-117">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a2b49-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a2b49-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2b49-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a2b49-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b49-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2b49-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a2b49-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2b49-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2b49-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




