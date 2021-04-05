---
title: Classe Win32_RDFileAssociation
description: Representa uma associação de tipo de arquivo para um RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDFileAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDFileAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918312"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="65446-105">\_Classe Win32 RDFileAssociation</span><span class="sxs-lookup"><span data-stu-id="65446-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="65446-106">Representa uma associação de tipo de arquivo para um RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="65446-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="65446-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="65446-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65446-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65446-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="65446-109">Membros</span><span class="sxs-lookup"><span data-stu-id="65446-109">Members</span></span>

<span data-ttu-id="65446-110">A classe **Win32 \_ RDFileAssociation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="65446-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="65446-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65446-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65446-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65446-112">Properties</span></span>

<span data-ttu-id="65446-113">A classe **Win32 \_ RDFileAssociation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="65446-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65446-114">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="65446-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65446-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65446-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65446-117">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="65446-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="65446-118">O nome da extensão de nome de arquivo, por exemplo,. txt.</span><span class="sxs-lookup"><span data-stu-id="65446-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="65446-119">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="65446-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-120">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="65446-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="65446-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65446-122">O conteúdo do ícone para esta associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="65446-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="65446-123">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="65446-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65446-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65446-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65446-126">O índice do ícone no arquivo.</span><span class="sxs-lookup"><span data-stu-id="65446-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="65446-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="65446-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65446-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65446-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65446-130">O caminho do arquivo para o ícone dessa associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="65446-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="65446-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="65446-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="65446-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="65446-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65446-134">Indica se essa associação é para um manipulador primário.</span><span class="sxs-lookup"><span data-stu-id="65446-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="65446-135">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="65446-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65446-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="65446-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65446-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65446-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65446-138">A dica para ajudar a abrir documentos com essa associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="65446-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65446-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65446-139">Requirements</span></span>



| <span data-ttu-id="65446-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="65446-140">Requirement</span></span> | <span data-ttu-id="65446-141">Valor</span><span class="sxs-lookup"><span data-stu-id="65446-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65446-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65446-142">Minimum supported client</span></span><br/> | <span data-ttu-id="65446-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="65446-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="65446-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65446-144">Minimum supported server</span></span><br/> | <span data-ttu-id="65446-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65446-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="65446-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="65446-146">Namespace</span></span><br/>                | <span data-ttu-id="65446-147">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="65446-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="65446-148">MOF</span><span class="sxs-lookup"><span data-stu-id="65446-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65446-149"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65446-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="65446-150">DLL</span><span class="sxs-lookup"><span data-stu-id="65446-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65446-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65446-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





