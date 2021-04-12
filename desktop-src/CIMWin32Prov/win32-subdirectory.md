---
description: A \_ classe WMI de associação de subdiretório Win32 relaciona um diretório (pasta) e um de seus subdiretórios (subpastas).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089454"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="21162-103">\_Classe de subdiretório Win32</span><span class="sxs-lookup"><span data-stu-id="21162-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="21162-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação de **\_ subdiretório Win32** relaciona um diretório (pasta) e um de seus subdiretórios (subpastas).</span><span class="sxs-lookup"><span data-stu-id="21162-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="21162-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="21162-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="21162-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="21162-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="21162-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21162-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="21162-108">Membros</span><span class="sxs-lookup"><span data-stu-id="21162-108">Members</span></span>

<span data-ttu-id="21162-109">A classe de **\_ subdiretório Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="21162-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="21162-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="21162-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21162-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="21162-111">Properties</span></span>

<span data-ttu-id="21162-112">A classe de **\_ subdiretório Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="21162-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21162-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="21162-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21162-114">Tipo de dados **: \_ diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="21162-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="21162-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="21162-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21162-116">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="21162-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="21162-117">Referência à instância que representa as propriedades do diretório pai (pasta) nesta associação.</span><span class="sxs-lookup"><span data-stu-id="21162-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="21162-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="21162-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21162-119">Tipo de dados **: \_ diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="21162-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="21162-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="21162-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21162-121">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório WMI Win32 \_ ")</span><span class="sxs-lookup"><span data-stu-id="21162-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="21162-122">Referência à instância que representa a parte de subdiretório (subpasta) da associação.</span><span class="sxs-lookup"><span data-stu-id="21162-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21162-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="21162-123">Remarks</span></span>

<span data-ttu-id="21162-124">A classe de **\_ subdiretório Win32** é derivada do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="21162-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="21162-125">Para retornar uma coleção de subpastas para uma pasta, crie uma consulta de associação que defina *ResultRole* como *PartComponent*.</span><span class="sxs-lookup"><span data-stu-id="21162-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="21162-126">Isso indica que todos os itens na coleção retornada devem desempenhar a função de um PartComponent, ou subpasta, do objeto Folder.</span><span class="sxs-lookup"><span data-stu-id="21162-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="21162-127">Para retornar a pasta pai de uma pasta, defina *ResultRole* como *GroupComponent*.</span><span class="sxs-lookup"><span data-stu-id="21162-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="21162-128">A classe de **\_ subdiretório Win32** funciona apenas no nível do sistema de arquivos imediatamente acima ou imediatamente abaixo da pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="21162-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="21162-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21162-129">Examples</span></span>

<span data-ttu-id="21162-130">O exemplo de VBScript a seguir retorna uma lista de todas as subpastas na pasta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="21162-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="21162-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21162-131">Requirements</span></span>



| <span data-ttu-id="21162-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="21162-132">Requirement</span></span> | <span data-ttu-id="21162-133">Valor</span><span class="sxs-lookup"><span data-stu-id="21162-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21162-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21162-134">Minimum supported client</span></span><br/> | <span data-ttu-id="21162-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21162-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21162-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21162-136">Minimum supported server</span></span><br/> | <span data-ttu-id="21162-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21162-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21162-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="21162-138">Namespace</span></span><br/>                | <span data-ttu-id="21162-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="21162-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21162-140">MOF</span><span class="sxs-lookup"><span data-stu-id="21162-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21162-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21162-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21162-142">DLL</span><span class="sxs-lookup"><span data-stu-id="21162-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21162-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21162-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21162-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="21162-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21162-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="21162-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="21162-146">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="21162-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
