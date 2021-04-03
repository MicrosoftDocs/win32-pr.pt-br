---
title: Método RemoveProgram da classe Win32_TSVirtualIP (Bdaiface. h)
description: Remove um programa da lista de programas que usam a virtualização de IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveProgram
- Método RemoveProgram Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645181"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="99041-106">Método RemoveProgram da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="99041-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="99041-107">Remove um programa da lista de programas que usam a virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="99041-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="99041-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99041-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="99041-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99041-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99041-110">*ProgramPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99041-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99041-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="99041-111">Type: **string**</span></span>

<span data-ttu-id="99041-112">O caminho e o nome do arquivo do programa a ser removido da lista.</span><span class="sxs-lookup"><span data-stu-id="99041-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="99041-113">Se o programa não for encontrado, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="99041-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99041-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99041-114">Return value</span></span>

<span data-ttu-id="99041-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="99041-115">Type: **uint32**</span></span>

<span data-ttu-id="99041-116">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="99041-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="99041-117">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="99041-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="99041-118">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="99041-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="99041-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99041-119">Requirements</span></span>



| <span data-ttu-id="99041-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="99041-120">Requirement</span></span> | <span data-ttu-id="99041-121">Valor</span><span class="sxs-lookup"><span data-stu-id="99041-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99041-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99041-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99041-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="99041-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="99041-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99041-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99041-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="99041-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="99041-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="99041-126">Namespace</span></span><br/>                | <span data-ttu-id="99041-127">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="99041-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="99041-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99041-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99041-129"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="99041-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="99041-130">MOF</span><span class="sxs-lookup"><span data-stu-id="99041-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99041-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99041-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="99041-132">DLL</span><span class="sxs-lookup"><span data-stu-id="99041-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99041-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99041-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99041-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="99041-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99041-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="99041-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





