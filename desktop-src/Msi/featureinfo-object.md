---
description: O objeto FeatureInfo contém informações sobre o recurso de destino e é criado a partir do objeto de sessão usando o método FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objeto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769321"
---
# <a name="featureinfo-object"></a><span data-ttu-id="ebe04-103">Objeto FeatureInfo</span><span class="sxs-lookup"><span data-stu-id="ebe04-103">FeatureInfo object</span></span>

<span data-ttu-id="ebe04-104">O objeto **FeatureInfo** contém informações sobre o recurso de destino e é criado a partir do objeto de [**sessão**](session-object.md) usando o método [**FeatureInfo**](session-featureinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ebe04-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="ebe04-105">Membros</span><span class="sxs-lookup"><span data-stu-id="ebe04-105">Members</span></span>

<span data-ttu-id="ebe04-106">O objeto **FeatureInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ebe04-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="ebe04-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ebe04-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebe04-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ebe04-108">Properties</span></span>

<span data-ttu-id="ebe04-109">O objeto **FeatureInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ebe04-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="ebe04-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ebe04-110">Property</span></span>                                                  | <span data-ttu-id="ebe04-111">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ebe04-111">Access type</span></span>           | <span data-ttu-id="ebe04-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebe04-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebe04-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="ebe04-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="ebe04-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ebe04-114">Read/write</span></span><br/> | <span data-ttu-id="ebe04-115">Retorna o valor do recurso na coluna atributos da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebe04-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="ebe04-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ebe04-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="ebe04-117">Retorna a descrição do recurso.</span><span class="sxs-lookup"><span data-stu-id="ebe04-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="ebe04-118">**Título**</span><span class="sxs-lookup"><span data-stu-id="ebe04-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="ebe04-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ebe04-119">Read-only</span></span><br/>  | <span data-ttu-id="ebe04-120">Retorna o título do recurso.</span><span class="sxs-lookup"><span data-stu-id="ebe04-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="ebe04-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebe04-121">Requirements</span></span>



| <span data-ttu-id="ebe04-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe04-122">Requirement</span></span> | <span data-ttu-id="ebe04-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ebe04-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe04-124">Versão</span><span class="sxs-lookup"><span data-stu-id="ebe04-124">Version</span></span><br/> | <span data-ttu-id="ebe04-125">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebe04-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ebe04-126">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebe04-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ebe04-127">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebe04-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ebe04-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ebe04-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ebe04-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebe04-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ebe04-130">IID</span><span class="sxs-lookup"><span data-stu-id="ebe04-130">IID</span></span><br/>     | <span data-ttu-id="ebe04-131">IID \_ IFeatureInfo é definido como 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ebe04-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="ebe04-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebe04-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe04-133">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ebe04-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




