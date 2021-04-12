---
title: Método SelectAllNetworkAdapters da classe Win32_TSNetworkAdapterSetting
description: O método SelectAllNetworkAdapters seleciona todos os adaptadores de rede.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectAllNetworkAdapters
- Método SelectAllNetworkAdapters Serviços de Área de Trabalho Remota, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota, método SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295821"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="320ca-106">Método SelectAllNetworkAdapters da classe Win32 \_ TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="320ca-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="320ca-107">O método **SelectAllNetworkAdapters** seleciona todos os adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="320ca-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="320ca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="320ca-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="320ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="320ca-109">Parameters</span></span>

<span data-ttu-id="320ca-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="320ca-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="320ca-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="320ca-111">Return value</span></span>

<span data-ttu-id="320ca-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="320ca-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="320ca-113">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="320ca-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="320ca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="320ca-114">Remarks</span></span>

<span data-ttu-id="320ca-115">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="320ca-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="320ca-116">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="320ca-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="320ca-117">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="320ca-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="320ca-118">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="320ca-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="320ca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="320ca-119">Requirements</span></span>



| <span data-ttu-id="320ca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="320ca-120">Requirement</span></span> | <span data-ttu-id="320ca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="320ca-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="320ca-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="320ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="320ca-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="320ca-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="320ca-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="320ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="320ca-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="320ca-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="320ca-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="320ca-126">Namespace</span></span><br/>                | <span data-ttu-id="320ca-127">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="320ca-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="320ca-128">MOF</span><span class="sxs-lookup"><span data-stu-id="320ca-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="320ca-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="320ca-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="320ca-130">DLL</span><span class="sxs-lookup"><span data-stu-id="320ca-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="320ca-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="320ca-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="320ca-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="320ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="320ca-133">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="320ca-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

