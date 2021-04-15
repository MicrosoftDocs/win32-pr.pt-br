---
description: Essa classe foi preterida. Em vez disso, recomendamos derivar da \_ classe de serviço CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760865"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="6f176-104">Classe do CIM \_ NetworkService</span><span class="sxs-lookup"><span data-stu-id="6f176-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="6f176-105">Essa classe foi preterida.</span><span class="sxs-lookup"><span data-stu-id="6f176-105">This class is deprecated.</span></span> <span data-ttu-id="6f176-106">Em vez disso, recomendamos derivar da classe de [**\_ serviço CIM**](cim-service.md) .</span><span class="sxs-lookup"><span data-stu-id="6f176-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f176-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f176-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="6f176-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6f176-108">Members</span></span>

<span data-ttu-id="6f176-109">A classe do **CIM \_ NetworkService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f176-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="6f176-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f176-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f176-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f176-111">Properties</span></span>

<span data-ttu-id="6f176-112">A classe do **CIM \_ NetworkService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f176-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f176-113">**Palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="6f176-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f176-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f176-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f176-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f176-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f176-116">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="6f176-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="6f176-117">Essa propriedade foi preterida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f176-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="6f176-118">Descrição preterida: uma matriz de palavras-chave que pode ser usada em consultas.</span><span class="sxs-lookup"><span data-stu-id="6f176-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f176-119">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="6f176-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f176-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f176-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f176-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f176-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f176-122">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")</span><span class="sxs-lookup"><span data-stu-id="6f176-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="6f176-123">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="6f176-123">This property is deprecated.</span></span> <span data-ttu-id="6f176-124">Em vez disso, recomendamos a classe **CIM \_ ServiceAccessURI** .</span><span class="sxs-lookup"><span data-stu-id="6f176-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="6f176-125">Descrição preterida: uma URL que fornece o protocolo, o local de rede e outras informações específicas do serviço necessárias para acessar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6f176-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f176-126">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="6f176-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f176-127">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f176-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f176-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f176-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f176-129">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="6f176-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="6f176-130">Essa propriedade foi preterida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f176-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="6f176-131">Descrição preterida: as pré-condições que devem ser atendidas para que esse serviço seja iniciado corretamente.</span><span class="sxs-lookup"><span data-stu-id="6f176-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f176-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="6f176-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f176-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f176-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f176-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f176-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f176-135">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")</span><span class="sxs-lookup"><span data-stu-id="6f176-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="6f176-136">Essa propriedade foi preterida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f176-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="6f176-137">Descrição preterida: os parâmetros que devem ser fornecidos ao método **StartService** para que esse serviço seja iniciado corretamente.</span><span class="sxs-lookup"><span data-stu-id="6f176-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f176-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f176-138">Requirements</span></span>



| <span data-ttu-id="6f176-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f176-139">Requirement</span></span> | <span data-ttu-id="6f176-140">Valor</span><span class="sxs-lookup"><span data-stu-id="6f176-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f176-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f176-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6f176-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6f176-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6f176-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f176-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6f176-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f176-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6f176-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f176-145">Namespace</span></span><br/>                | <span data-ttu-id="6f176-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6f176-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f176-147">MOF</span><span class="sxs-lookup"><span data-stu-id="6f176-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f176-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f176-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f176-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6f176-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f176-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f176-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f176-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f176-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f176-152">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="6f176-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

