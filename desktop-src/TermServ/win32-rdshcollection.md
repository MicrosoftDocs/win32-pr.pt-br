---
title: Classe Win32_RDSHCollection
description: Gerencia uma coleção de hosts de sessão de Área de Trabalho Remota.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDSHCollection Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDSHCollection classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455267"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="01c0b-105">\_Classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="01c0b-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="01c0b-106">Gerencia uma coleção de hosts de sessão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="01c0b-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="01c0b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01c0b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c0b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01c0b-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="01c0b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="01c0b-109">Members</span></span>

<span data-ttu-id="01c0b-110">A classe **Win32 \_ RDSHCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01c0b-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="01c0b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="01c0b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="01c0b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01c0b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01c0b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="01c0b-113">Methods</span></span>

<span data-ttu-id="01c0b-114">A classe **Win32 \_ RDSHCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="01c0b-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="01c0b-115">Método</span><span class="sxs-lookup"><span data-stu-id="01c0b-115">Method</span></span>                                                                      | <span data-ttu-id="01c0b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01c0b-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01c0b-117">**Getint32property**</span><span class="sxs-lookup"><span data-stu-id="01c0b-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="01c0b-118">Recupera um valor da propriedade Integer de um objeto **\_ RDSHCollection do Win32** .</span><span class="sxs-lookup"><span data-stu-id="01c0b-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="01c0b-119">**Getstringproperty**</span><span class="sxs-lookup"><span data-stu-id="01c0b-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="01c0b-120">Recupera um valor de propriedade da cadeia de caracteres de um objeto **\_ RDSHCollection do Win32** .</span><span class="sxs-lookup"><span data-stu-id="01c0b-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="01c0b-121">**KeyValueCompareAndSet**</span><span class="sxs-lookup"><span data-stu-id="01c0b-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="01c0b-122">Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor.</span><span class="sxs-lookup"><span data-stu-id="01c0b-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="01c0b-123">Se a chave não existir, o método irá inserir a chave na coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="01c0b-124">**KeyValueDelete**</span><span class="sxs-lookup"><span data-stu-id="01c0b-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="01c0b-125">Exclui a chave especificada (e o valor associado) da coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="01c0b-126">**KeyValueGet**</span><span class="sxs-lookup"><span data-stu-id="01c0b-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="01c0b-127">Recupera o valor associado à chave especificada na coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="01c0b-128">**Setint32property**</span><span class="sxs-lookup"><span data-stu-id="01c0b-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="01c0b-129">Atualiza um valor da propriedade Integer de um objeto **\_ RDSHCollection do Win32** .</span><span class="sxs-lookup"><span data-stu-id="01c0b-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="01c0b-130">**Setstringproperty**</span><span class="sxs-lookup"><span data-stu-id="01c0b-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="01c0b-131">Atualiza um valor de propriedade de cadeia de caracteres de um objeto **Win32 \_ RDSHCollection** .</span><span class="sxs-lookup"><span data-stu-id="01c0b-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="01c0b-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01c0b-132">Properties</span></span>

<span data-ttu-id="01c0b-133">A classe **Win32 \_ RDSHCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01c0b-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01c0b-134">**Alias**</span><span class="sxs-lookup"><span data-stu-id="01c0b-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01c0b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01c0b-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01c0b-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-138">Obtém e define o alias da coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="01c0b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01c0b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01c0b-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-142">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01c0b-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-143">Obtém e define a descrição da coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="01c0b-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01c0b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01c0b-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-147">Obtém e define o nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="01c0b-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="01c0b-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c0b-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01c0b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01c0b-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01c0b-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01c0b-151">**Windows server 2012 R2 e Windows server 2012:** Essa propriedade não está disponível antes do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="01c0b-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="01c0b-152">O tipo de coleção.</span><span class="sxs-lookup"><span data-stu-id="01c0b-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="01c0b-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span><span class="sxs-lookup"><span data-stu-id="01c0b-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="01c0b-154">(2)</span><span class="sxs-lookup"><span data-stu-id="01c0b-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="01c0b-155">Reservado</span><span class="sxs-lookup"><span data-stu-id="01c0b-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="01c0b-156">(3)</span><span class="sxs-lookup"><span data-stu-id="01c0b-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="01c0b-157">Reservado</span><span class="sxs-lookup"><span data-stu-id="01c0b-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="01c0b-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span><span class="sxs-lookup"><span data-stu-id="01c0b-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="01c0b-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Pessoa física** (5)</span><span class="sxs-lookup"><span data-stu-id="01c0b-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="01c0b-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="01c0b-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="01c0b-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01c0b-161">Requirements</span></span>



| <span data-ttu-id="01c0b-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c0b-162">Requirement</span></span> | <span data-ttu-id="01c0b-163">Valor</span><span class="sxs-lookup"><span data-stu-id="01c0b-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c0b-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01c0b-164">Minimum supported client</span></span><br/> | <span data-ttu-id="01c0b-165">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="01c0b-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="01c0b-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01c0b-166">Minimum supported server</span></span><br/> | <span data-ttu-id="01c0b-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01c0b-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="01c0b-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="01c0b-168">Namespace</span></span><br/>                | <span data-ttu-id="01c0b-169">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="01c0b-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="01c0b-170">MOF</span><span class="sxs-lookup"><span data-stu-id="01c0b-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01c0b-171"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01c0b-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="01c0b-172">DLL</span><span class="sxs-lookup"><span data-stu-id="01c0b-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c0b-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c0b-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="01c0b-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="01c0b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c0b-175">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="01c0b-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

