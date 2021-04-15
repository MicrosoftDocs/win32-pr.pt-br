---
title: Método setprogramlist da classe Win32_TSVirtualIP
description: Substitui a lista de programas que usam a virtualização de IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Método setprogramlist Serviços de Área de Trabalho Remota
- Método setprogramlist Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método setprogramalist
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499456"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="8939f-106">Método setprogramlist da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="8939f-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="8939f-107">Substitui a lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="8939f-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="8939f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8939f-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="8939f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8939f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8939f-110">*Programalist* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8939f-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8939f-111">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8939f-111">Type: **string\[\]**</span></span>

<span data-ttu-id="8939f-112">Uma matriz de cadeias de caracteres que contém os nomes de arquivo e caminho dos programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="8939f-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8939f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8939f-113">Return value</span></span>

<span data-ttu-id="8939f-114">Tipo: não **Int32**</span><span class="sxs-lookup"><span data-stu-id="8939f-114">Type: **unint32**</span></span>

<span data-ttu-id="8939f-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="8939f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8939f-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="8939f-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8939f-117">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8939f-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="8939f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8939f-118">Requirements</span></span>



| <span data-ttu-id="8939f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8939f-119">Requirement</span></span> | <span data-ttu-id="8939f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8939f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8939f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8939f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8939f-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8939f-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8939f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8939f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8939f-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8939f-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8939f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8939f-125">Namespace</span></span><br/>                | <span data-ttu-id="8939f-126">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8939f-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8939f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8939f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8939f-128"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8939f-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8939f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8939f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8939f-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8939f-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8939f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8939f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8939f-132">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="8939f-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





