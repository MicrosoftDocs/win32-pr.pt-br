---
description: ICE74 verifica se a propriedade FASTOEM não foi criada na tabela de propriedades.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749588"
---
# <a name="ice74"></a><span data-ttu-id="c85c2-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="c85c2-103">ICE74</span></span>

<span data-ttu-id="c85c2-104">ICE74 verifica se a propriedade [**FASTOEM**](fastoem.md) não foi criada na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c85c2-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="c85c2-105">A propriedade [**FASTOEM**](fastoem.md) permite que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="c85c2-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="c85c2-106">Ele não pode ser usado após a primeira instalação.</span><span class="sxs-lookup"><span data-stu-id="c85c2-106">It cannot be used after the first install.</span></span> <span data-ttu-id="c85c2-107">A propriedade **FASTOEM** não deve ser criada na tabela de propriedades porque ela interfere nas instalações subsequentes para a manutenção, remoção ou reparo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c85c2-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="c85c2-108">ICE74 também verifica se a propriedade [**UpgradeCode**](upgradecode.md) é criada na [tabela de propriedades](property-table.md)e se seu valor não é um GUID nulo, {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="c85c2-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="c85c2-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="c85c2-109">Result</span></span>

<span data-ttu-id="c85c2-110">ICE74 pode postar os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c85c2-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="c85c2-111">Erro de ICE74</span><span class="sxs-lookup"><span data-stu-id="c85c2-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="c85c2-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c85c2-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85c2-113">A propriedade [**FASTOEM**](fastoem.md) não pode ser criada na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="c85c2-114">A propriedade [**FASTOEM**](fastoem.md) foi definida na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="c85c2-115">' \[ 2 \] ' não é um [**UpgradeCode**](upgradecode.md)válido.</span><span class="sxs-lookup"><span data-stu-id="c85c2-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="c85c2-116">Um GUID nulo foi inserido para a propriedade [**UpgradeCode**](upgradecode.md) na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="c85c2-117">ICE74 pode postar o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="c85c2-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="c85c2-118">Aviso de ICE74</span><span class="sxs-lookup"><span data-stu-id="c85c2-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="c85c2-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c85c2-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c85c2-120">A propriedade [**UpgradeCode**](upgradecode.md) não foi criada na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="c85c2-121">É altamente recomendável que os autores de pacotes de instalação especifiquem um **UpgradeCode** para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c85c2-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="c85c2-122">A propriedade [**UpgradeCode**](upgradecode.md) não foi criada na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="c85c2-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c85c2-123">Example</span></span>

<span data-ttu-id="c85c2-124">ICE74 relata o seguinte erro se a propriedade [**FASTOEM**](fastoem.md) estiver definida: o FASTOEM</span><span class="sxs-lookup"><span data-stu-id="c85c2-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="c85c2-125">[Tabela de propriedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c85c2-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="c85c2-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c85c2-126">Property</span></span>                   | <span data-ttu-id="c85c2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c85c2-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="c85c2-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="c85c2-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="c85c2-129">1</span><span class="sxs-lookup"><span data-stu-id="c85c2-129">1</span></span>     |



 

<span data-ttu-id="c85c2-130">Para corrigir esse erro, remova a propriedade [**FASTOEM**](fastoem.md) da tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c85c2-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c85c2-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c85c2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c85c2-132">**Propriedade FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="c85c2-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="c85c2-133">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="c85c2-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="c85c2-134">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="c85c2-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



