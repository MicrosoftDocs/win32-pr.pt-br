---
description: A interface IProvidePropertyBuilder, quando implementada, permite que os objetos especifiquem objetos do construtor de propriedades para propriedades.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interface IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752768"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="41ccc-103">Interface IProvidePropertyBuilder</span><span class="sxs-lookup"><span data-stu-id="41ccc-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="41ccc-104">A interface **IProvidePropertyBuilder** , quando implementada, permite que os objetos especifiquem objetos do construtor de propriedades para propriedades.</span><span class="sxs-lookup"><span data-stu-id="41ccc-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="41ccc-105">Os construtores são invocados por um botão de reticências ( \[ ... \] ) no navegador de propriedades Microsoft Visual Studio e é invocado por meio de [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quando o botão é pressionado.</span><span class="sxs-lookup"><span data-stu-id="41ccc-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="41ccc-106">Para fornecer um construtor para uma determinada propriedade, retorne um GUID para o construtor de propriedades que deve ser invocado para a propriedade atual de [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="41ccc-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="41ccc-107">Os construtores geralmente são implementados por meio de caixas de diálogo modais.</span><span class="sxs-lookup"><span data-stu-id="41ccc-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="41ccc-108">A versão desta interface é 1,0.</span><span class="sxs-lookup"><span data-stu-id="41ccc-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="41ccc-109">As chamadas de método são recebidas em um ponto de extremidade atribuído dinamicamente (conforme descrito na documentação binária do MSMQ no mapeamento de ponto de extremidade) e usam o UUID (identificador universal exclusivo) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span><span class="sxs-lookup"><span data-stu-id="41ccc-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="41ccc-110">Membros</span><span class="sxs-lookup"><span data-stu-id="41ccc-110">Members</span></span>

<span data-ttu-id="41ccc-111">A interface **IProvidePropertyBuilder: IUnknown** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="41ccc-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="41ccc-112">**IProvidePropertyBuilder** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41ccc-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="41ccc-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="41ccc-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="41ccc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="41ccc-114">Methods</span></span>

<span data-ttu-id="41ccc-115">A interface **IProvidePropertyBuilder: IUnknown** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="41ccc-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="41ccc-116">Método</span><span class="sxs-lookup"><span data-stu-id="41ccc-116">Method</span></span>                                                                       | <span data-ttu-id="41ccc-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="41ccc-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41ccc-118">**ExecuteBuilder**</span><span class="sxs-lookup"><span data-stu-id="41ccc-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="41ccc-119">Notifica um objeto de que ele deve exibir seu construtor para a propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="41ccc-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="41ccc-120">**MapPropertyToBuilder**</span><span class="sxs-lookup"><span data-stu-id="41ccc-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="41ccc-121">Verifica se um construtor deve ser associado a uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="41ccc-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="41ccc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ccc-122">Requirements</span></span>



| <span data-ttu-id="41ccc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ccc-123">Requirement</span></span> | <span data-ttu-id="41ccc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="41ccc-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41ccc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="41ccc-125">DLL</span></span><br/> | <dl> <span data-ttu-id="41ccc-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41ccc-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
