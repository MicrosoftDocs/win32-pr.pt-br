---
title: Método FileExtensions da classe Win32_TSApplicationFileExtensions
description: Fornece uma lista das extensões de nome de arquivo que são manipuladas por um aplicativo.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Método de extensões de fileServiços de Área de Trabalho Remota
- Método de extensões de fileServiços de Área de Trabalho Remota, classe Win32_TSApplicationFileExtensions
- Classe de Win32_TSApplicationFileExtensions Serviços de Área de Trabalho Remota, método FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919047"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="0f444-106">Método FileExtensions da classe Win32 \_ TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="0f444-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="0f444-107">Fornece uma lista das extensões de nome de arquivo que são manipuladas por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f444-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f444-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f444-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="0f444-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f444-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f444-110">*AppPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f444-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f444-111">O caminho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f444-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="0f444-112">*Extensões* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0f444-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f444-113">As extensões de nome de arquivo que são manipuladas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f444-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f444-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f444-114">Remarks</span></span>

<span data-ttu-id="0f444-115">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0f444-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0f444-116">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0f444-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f444-117">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0f444-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f444-118">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0f444-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f444-119">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0f444-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f444-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f444-120">Requirements</span></span>



| <span data-ttu-id="0f444-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f444-121">Requirement</span></span> | <span data-ttu-id="0f444-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0f444-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f444-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f444-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f444-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0f444-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0f444-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f444-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f444-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f444-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f444-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f444-127">Namespace</span></span><br/>                | <span data-ttu-id="0f444-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="0f444-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0f444-129">MOF</span><span class="sxs-lookup"><span data-stu-id="0f444-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f444-130"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f444-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0f444-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0f444-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f444-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f444-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f444-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f444-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f444-134">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="0f444-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

