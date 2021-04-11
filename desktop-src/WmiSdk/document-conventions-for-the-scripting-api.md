---
description: Descreve as convenções de documento para a leitura de tópicos da API de script do WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Convenções de documento para a API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296997"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="80869-103">Convenções de documento para a API de script</span><span class="sxs-lookup"><span data-stu-id="80869-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="80869-104">A [API de script para referência de WMI](scripting-api-for-wmi.md) usa as seguintes convenções de documento:</span><span class="sxs-lookup"><span data-stu-id="80869-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="80869-105">Os tipos de parâmetro são definidos usando um prefixo: b (booliano), Str (String), I (Integer), obj (Automation Object), var (Variant).</span><span class="sxs-lookup"><span data-stu-id="80869-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="80869-106">Os parâmetros opcionais são colocados entre colchetes com seus valores padrão mostrados pela atribuição.</span><span class="sxs-lookup"><span data-stu-id="80869-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="80869-107">No caso de parâmetros de objeto, os caracteres após o prefixo "obj" indicam o tipo de objeto esperado.</span><span class="sxs-lookup"><span data-stu-id="80869-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="80869-108">Parâmetro de objeto</span><span class="sxs-lookup"><span data-stu-id="80869-108">Object parameter</span></span>      | <span data-ttu-id="80869-109">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="80869-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="80869-110">*WbemDatetime*</span><span class="sxs-lookup"><span data-stu-id="80869-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="80869-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="80869-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="80869-112">*WbemEventSource*</span><span class="sxs-lookup"><span data-stu-id="80869-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="80869-113">**SWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="80869-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="80869-114">*WbemLocator*</span><span class="sxs-lookup"><span data-stu-id="80869-114">*WbemLocator*</span></span>         | [<span data-ttu-id="80869-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="80869-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="80869-116">*WbemMethod*</span><span class="sxs-lookup"><span data-stu-id="80869-116">*WbemMethod*</span></span>          | [<span data-ttu-id="80869-117">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="80869-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="80869-118">*WbemMethodSet*</span><span class="sxs-lookup"><span data-stu-id="80869-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="80869-119">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="80869-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="80869-120">*WbemNamedValueSet*</span><span class="sxs-lookup"><span data-stu-id="80869-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="80869-121">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="80869-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="80869-122">*WbemObject*</span><span class="sxs-lookup"><span data-stu-id="80869-122">*WbemObject*</span></span>          | [<span data-ttu-id="80869-123">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="80869-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="80869-124">*WbemObjectEx*</span><span class="sxs-lookup"><span data-stu-id="80869-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="80869-125">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="80869-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="80869-126">*WbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="80869-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="80869-127">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="80869-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="80869-128">*WbemObjectSet*</span><span class="sxs-lookup"><span data-stu-id="80869-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="80869-129">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="80869-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="80869-130">*WbemPrivilege*</span><span class="sxs-lookup"><span data-stu-id="80869-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="80869-131">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="80869-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="80869-132">*WbemPrivilegeSet*</span><span class="sxs-lookup"><span data-stu-id="80869-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="80869-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="80869-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="80869-134">*WbemProperty*</span><span class="sxs-lookup"><span data-stu-id="80869-134">*WbemProperty*</span></span>        | [<span data-ttu-id="80869-135">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="80869-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="80869-136">*WbemPropertySet*</span><span class="sxs-lookup"><span data-stu-id="80869-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="80869-137">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="80869-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="80869-138">*WbemQualifier*</span><span class="sxs-lookup"><span data-stu-id="80869-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="80869-139">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="80869-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="80869-140">*WbemQualifierSet*</span><span class="sxs-lookup"><span data-stu-id="80869-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="80869-141">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="80869-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="80869-142">*WbemRefreshableItem*</span><span class="sxs-lookup"><span data-stu-id="80869-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="80869-143">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="80869-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="80869-144">*WbemRefresher*</span><span class="sxs-lookup"><span data-stu-id="80869-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="80869-145">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="80869-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="80869-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="80869-146">*WbemServices*</span></span>        | [<span data-ttu-id="80869-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="80869-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="80869-148">*WbemServicesEx*</span><span class="sxs-lookup"><span data-stu-id="80869-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="80869-149">**SWbemServicesEx**</span><span class="sxs-lookup"><span data-stu-id="80869-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="80869-150">Por exemplo, o código a seguir mostra como nomear variáveis para diferentes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="80869-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



