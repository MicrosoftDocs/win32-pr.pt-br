---
title: Método addprogram da classe Win32_TSVirtualIP (Bdaiface. h)
description: Adiciona um programa à lista de programas que usam a virtualização de IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Método addprogram Serviços de Área de Trabalho Remota
- Método addprogram Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método addprogram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644466"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="a6460-106">Método addprogram da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a6460-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="a6460-107">Adiciona um programa à lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="a6460-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6460-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6460-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="a6460-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6460-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6460-110">*ProgramPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6460-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6460-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a6460-111">Type: **string**</span></span>

<span data-ttu-id="a6460-112">O caminho e o nome do arquivo do programa a ser adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="a6460-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6460-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6460-113">Return value</span></span>

<span data-ttu-id="a6460-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6460-114">Type: **uint32**</span></span>

<span data-ttu-id="a6460-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a6460-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a6460-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a6460-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a6460-117">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a6460-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6460-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6460-118">Requirements</span></span>



| <span data-ttu-id="a6460-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6460-119">Requirement</span></span> | <span data-ttu-id="a6460-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6460-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6460-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6460-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6460-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6460-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a6460-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6460-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6460-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6460-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a6460-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6460-125">Namespace</span></span><br/>                | <span data-ttu-id="a6460-126">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a6460-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a6460-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6460-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6460-128"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6460-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6460-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a6460-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6460-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6460-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6460-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a6460-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6460-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6460-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6460-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6460-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6460-134">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="a6460-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





