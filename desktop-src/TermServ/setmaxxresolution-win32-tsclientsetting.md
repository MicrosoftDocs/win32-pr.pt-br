---
title: Método SetMaxXResolution da classe Win32_TSClientSetting
description: Define a propriedade MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxXResolution
- Método SetMaxXResolution Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455045"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="a4a91-106">Método SetMaxXResolution da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="a4a91-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="a4a91-107">Define a propriedade **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="a4a91-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a91-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a91-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="a4a91-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4a91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4a91-110">*MaxXResolution* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4a91-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4a91-111">A nova resolução máxima de X com suporte do servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a91-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="a4a91-112">O valor mínimo é 200 e o valor máximo é 4096.</span><span class="sxs-lookup"><span data-stu-id="a4a91-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4a91-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4a91-113">Return value</span></span>

<span data-ttu-id="a4a91-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a4a91-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a4a91-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a4a91-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a4a91-116">O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="a4a91-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a91-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4a91-117">Requirements</span></span>



| <span data-ttu-id="a4a91-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a91-118">Requirement</span></span> | <span data-ttu-id="a4a91-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a91-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a91-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a91-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a91-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a4a91-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a4a91-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4a91-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a91-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4a91-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a4a91-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4a91-124">Namespace</span></span><br/>                | <span data-ttu-id="a4a91-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a4a91-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a4a91-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a4a91-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4a91-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4a91-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4a91-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a91-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a91-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a91-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4a91-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4a91-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4a91-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a4a91-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





