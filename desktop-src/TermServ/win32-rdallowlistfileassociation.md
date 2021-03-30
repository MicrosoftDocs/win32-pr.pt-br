---
title: Classe Win32_RDAllowListFileAssociation
description: Descreve uma associação de tipo de arquivo publicado com um RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDAllowListFileAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDAllowListFileAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455140"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="e2709-105">\_Classe Win32 RDAllowListFileAssociation</span><span class="sxs-lookup"><span data-stu-id="e2709-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="e2709-106">Descreve uma associação de tipo de arquivo publicado com um RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e2709-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="e2709-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e2709-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2709-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2709-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="e2709-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e2709-109">Members</span></span>

<span data-ttu-id="e2709-110">A classe **Win32 \_ RDAllowListFileAssociation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2709-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="e2709-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2709-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2709-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2709-112">Properties</span></span>

<span data-ttu-id="e2709-113">A classe **Win32 \_ RDAllowListFileAssociation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2709-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2709-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="e2709-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2709-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2709-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2709-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e2709-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2709-117">Alias do RemoteApp associado à extensão.</span><span class="sxs-lookup"><span data-stu-id="e2709-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="e2709-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="e2709-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2709-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2709-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2709-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e2709-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e2709-121">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e2709-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2709-122">Nome da extensão, por exemplo,. txt.</span><span class="sxs-lookup"><span data-stu-id="e2709-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="e2709-123">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="e2709-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2709-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e2709-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2709-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e2709-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e2709-126">Dica para ajudar a abrir documentos com esta associação de arquivo</span><span class="sxs-lookup"><span data-stu-id="e2709-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2709-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2709-127">Requirements</span></span>



| <span data-ttu-id="e2709-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2709-128">Requirement</span></span> | <span data-ttu-id="e2709-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e2709-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2709-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2709-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2709-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e2709-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e2709-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2709-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2709-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e2709-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="e2709-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2709-134">Namespace</span></span><br/>                | <span data-ttu-id="e2709-135">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e2709-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e2709-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e2709-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2709-137"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2709-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e2709-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e2709-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2709-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2709-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





