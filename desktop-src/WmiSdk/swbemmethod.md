---
description: Você pode usar as propriedades do objeto SWbemMethod para inspecionar uma única definição de método de um objeto WMI. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objeto SWbemMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505672"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="611df-104">Objeto SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="611df-104">SWbemMethod object</span></span>

<span data-ttu-id="611df-105">Você pode usar as propriedades do objeto **SWbemMethod** para inspecionar uma única definição de método de um objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="611df-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="611df-106">Este objeto não pode ser criado pela chamada VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="611df-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="611df-107">Esse objeto pode ser usado para inspecionar as definições de métodos.</span><span class="sxs-lookup"><span data-stu-id="611df-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="611df-108">Para invocar os métodos, você deve usar o acesso direto (consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md)) em um objeto [**SWbemObject**](swbemobject.md) (que é o mecanismo recomendado) ou a chamada de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="611df-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="611df-109">Nesta versão da API, não há suporte para o acesso de gravação para informações de método.</span><span class="sxs-lookup"><span data-stu-id="611df-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="611df-110">Se você quiser definir métodos ou modificar definições de método existentes, poderá definir as alterações de método em um arquivo MOF e enviar as alterações usando o [compilador MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="611df-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="611df-111">Como alternativa, use a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="611df-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="611df-112">Membros</span><span class="sxs-lookup"><span data-stu-id="611df-112">Members</span></span>

<span data-ttu-id="611df-113">O objeto **SWbemMethod** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="611df-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="611df-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="611df-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="611df-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="611df-115">Properties</span></span>

<span data-ttu-id="611df-116">O objeto **SWbemMethod** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="611df-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="611df-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="611df-117">Property</span></span>                                                      | <span data-ttu-id="611df-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="611df-118">Access type</span></span>          | <span data-ttu-id="611df-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="611df-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="611df-120">**Inparâmetros**</span><span class="sxs-lookup"><span data-stu-id="611df-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="611df-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="611df-121">Read-only</span></span><br/> | <span data-ttu-id="611df-122">Um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de entrada para esse método.</span><span class="sxs-lookup"><span data-stu-id="611df-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="611df-123">**Nome**</span><span class="sxs-lookup"><span data-stu-id="611df-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="611df-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="611df-124">Read-only</span></span><br/> | <span data-ttu-id="611df-125">O nome do método.</span><span class="sxs-lookup"><span data-stu-id="611df-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="611df-126">**Ter**</span><span class="sxs-lookup"><span data-stu-id="611df-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="611df-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="611df-127">Read-only</span></span><br/> | <span data-ttu-id="611df-128">Classe de origem do método.</span><span class="sxs-lookup"><span data-stu-id="611df-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="611df-129">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="611df-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="611df-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="611df-130">Read-only</span></span><br/> | <span data-ttu-id="611df-131">Um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de saída e o tipo de retorno desse método.</span><span class="sxs-lookup"><span data-stu-id="611df-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="611df-132">**Qualificadores\_**</span><span class="sxs-lookup"><span data-stu-id="611df-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="611df-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="611df-133">Read-only</span></span><br/> | <span data-ttu-id="611df-134">Um objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contém os qualificadores para este método.</span><span class="sxs-lookup"><span data-stu-id="611df-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="611df-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="611df-135">Requirements</span></span>



| <span data-ttu-id="611df-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="611df-136">Requirement</span></span> | <span data-ttu-id="611df-137">Valor</span><span class="sxs-lookup"><span data-stu-id="611df-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="611df-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="611df-138">Minimum supported client</span></span><br/> | <span data-ttu-id="611df-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="611df-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="611df-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="611df-140">Minimum supported server</span></span><br/> | <span data-ttu-id="611df-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="611df-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="611df-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="611df-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="611df-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="611df-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="611df-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="611df-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="611df-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="611df-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="611df-146">DLL</span><span class="sxs-lookup"><span data-stu-id="611df-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="611df-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="611df-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="611df-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="611df-148">CLSID</span></span><br/>                    | <span data-ttu-id="611df-149">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="611df-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="611df-150">IID</span><span class="sxs-lookup"><span data-stu-id="611df-150">IID</span></span><br/>                      | <span data-ttu-id="611df-151">ISWbemMethod de IID \_</span><span class="sxs-lookup"><span data-stu-id="611df-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="611df-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="611df-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611df-153">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="611df-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




