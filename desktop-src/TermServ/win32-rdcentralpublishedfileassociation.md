---
title: Classe Win32_RDCentralPublishedFileAssociation
description: Informações de uma extensão de arquivo associada a um aplicativo.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedFileAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedFileAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455857"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="2b6fb-105">\_Classe Win32 RDCentralPublishedFileAssociation</span><span class="sxs-lookup"><span data-stu-id="2b6fb-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="2b6fb-106">Informações para uma extensão de arquivo associada a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="2b6fb-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="2b6fb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6fb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b6fb-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="2b6fb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2b6fb-109">Members</span></span>

<span data-ttu-id="2b6fb-110">A classe **Win32 \_ RDCentralPublishedFileAssociation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b6fb-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="2b6fb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b6fb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b6fb-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b6fb-112">Properties</span></span>

<span data-ttu-id="2b6fb-113">A classe **Win32 \_ RDCentralPublishedFileAssociation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b6fb-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b6fb-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-117">Alias do RemoteApp da Associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="2b6fb-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b6fb-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-121">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b6fb-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-122">Nome da extensão (por exemplo,. txt).</span><span class="sxs-lookup"><span data-stu-id="2b6fb-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="2b6fb-123">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b6fb-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-126">Alias do farm RemoteApp's da Associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="2b6fb-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="2b6fb-127">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-128">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b6fb-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-130">Conteúdo do ícone para esta associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="2b6fb-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b6fb-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-134">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-134">Reserved for future use.</span></span> <span data-ttu-id="2b6fb-135">Será sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="2b6fb-136">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6fb-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2b6fb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6fb-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2b6fb-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2b6fb-139">Dica para ajudar a abrir documentos com essa associação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2b6fb-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b6fb-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b6fb-140">Requirements</span></span>



| <span data-ttu-id="2b6fb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6fb-141">Requirement</span></span> | <span data-ttu-id="2b6fb-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2b6fb-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6fb-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b6fb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6fb-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b6fb-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2b6fb-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b6fb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6fb-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b6fb-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="2b6fb-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b6fb-147">Namespace</span></span><br/>                | <span data-ttu-id="2b6fb-148">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2b6fb-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2b6fb-149">MOF</span><span class="sxs-lookup"><span data-stu-id="2b6fb-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b6fb-150"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fb-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2b6fb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6fb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b6fb-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fb-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

