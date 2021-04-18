---
title: Método SetMaxYResolution da classe Win32_TSClientSetting
description: Define a propriedade MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxYResolution
- Método SetMaxYResolution Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757187"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="9f14d-106">Método SetMaxYResolution da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="9f14d-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="9f14d-107">Define a propriedade **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="9f14d-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f14d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f14d-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="9f14d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f14d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f14d-110">*MaxYResolution* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f14d-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f14d-111">A nova resolução de Y máxima com suporte do servidor.</span><span class="sxs-lookup"><span data-stu-id="9f14d-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="9f14d-112">O valor mínimo é 200 e o valor máximo é 2048.</span><span class="sxs-lookup"><span data-stu-id="9f14d-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f14d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f14d-113">Return value</span></span>

<span data-ttu-id="9f14d-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="9f14d-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9f14d-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="9f14d-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="9f14d-116">O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="9f14d-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f14d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f14d-117">Requirements</span></span>



| <span data-ttu-id="9f14d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f14d-118">Requirement</span></span> | <span data-ttu-id="9f14d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9f14d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f14d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f14d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f14d-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f14d-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9f14d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f14d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f14d-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f14d-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9f14d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f14d-124">Namespace</span></span><br/>                | <span data-ttu-id="9f14d-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9f14d-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9f14d-126">MOF</span><span class="sxs-lookup"><span data-stu-id="9f14d-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f14d-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f14d-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f14d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9f14d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f14d-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f14d-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f14d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f14d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f14d-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9f14d-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





