---
title: Classe Win32_RDMSFileTypeAssociation
description: Gerencia uma associação de tipo de arquivo para um aplicativo publicado.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSFileTypeAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSFileTypeAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369269"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="2fccb-105">\_Classe Win32 RDMSFileTypeAssociation</span><span class="sxs-lookup"><span data-stu-id="2fccb-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="2fccb-106">Gerencia uma associação de tipo de arquivo para um aplicativo publicado.</span><span class="sxs-lookup"><span data-stu-id="2fccb-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="2fccb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2fccb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fccb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fccb-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="2fccb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2fccb-109">Members</span></span>

<span data-ttu-id="2fccb-110">A classe **Win32 \_ RDMSFileTypeAssociation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2fccb-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="2fccb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2fccb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fccb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2fccb-112">Properties</span></span>

<span data-ttu-id="2fccb-113">A classe **Win32 \_ RDMSFileTypeAssociation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2fccb-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fccb-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="2fccb-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fccb-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fccb-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-118">Obtém e define o alias do aplicativo que está associado ao tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-119">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="2fccb-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fccb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2fccb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fccb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-123">Obtém o nome da extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-124">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="2fccb-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-125">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="2fccb-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-127">Obtém e define o conteúdo do ícone para o tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="2fccb-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fccb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-131">Obtém e define o índice para o ícone do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="2fccb-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fccb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-135">Obtém e define o caminho para o ícone do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-136">**IsPrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="2fccb-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2fccb-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-139">Obtém e define um valor que indica se a associação de tipo de arquivo é para o manipulador primário.</span><span class="sxs-lookup"><span data-stu-id="2fccb-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="2fccb-140">**True** se a associação de tipo de arquivo for para o manipulador primário; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2fccb-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="2fccb-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-142">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2fccb-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-144">Se este FTAS é publicado.</span><span class="sxs-lookup"><span data-stu-id="2fccb-144">Whether this FTA is published.</span></span>

<span data-ttu-id="2fccb-145">Obtém e define um valor que indica se a associação de tipo de arquivo é publicada.</span><span class="sxs-lookup"><span data-stu-id="2fccb-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="2fccb-146">**True** se a associação de tipo de arquivo for publicada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2fccb-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="2fccb-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fccb-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2fccb-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-150">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fccb-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-151">Obtém e define o nome do pool de aplicativos para a associação de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="2fccb-152">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="2fccb-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fccb-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fccb-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fccb-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2fccb-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fccb-155">Obtém uma dica para ajudar os usuários a abrir a extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2fccb-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fccb-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fccb-156">Requirements</span></span>



| <span data-ttu-id="2fccb-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fccb-157">Requirement</span></span> | <span data-ttu-id="2fccb-158">Valor</span><span class="sxs-lookup"><span data-stu-id="2fccb-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fccb-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fccb-159">Minimum supported client</span></span><br/> | <span data-ttu-id="2fccb-160">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2fccb-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2fccb-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fccb-161">Minimum supported server</span></span><br/> | <span data-ttu-id="2fccb-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fccb-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2fccb-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fccb-163">Namespace</span></span><br/>                | <span data-ttu-id="2fccb-164">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="2fccb-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2fccb-165">MOF</span><span class="sxs-lookup"><span data-stu-id="2fccb-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fccb-166"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fccb-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fccb-167">DLL</span><span class="sxs-lookup"><span data-stu-id="2fccb-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fccb-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fccb-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2fccb-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fccb-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fccb-170">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2fccb-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

