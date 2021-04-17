---
title: Método SetMaxMonitors da classe Win32_TSClientSetting
description: Define a propriedade MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxMonitors
- Método SetMaxMonitors Serviços de Área de Trabalho Remota, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Serviços de Área de Trabalho Remota, método SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769377"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="81b6b-106">Método SetMaxMonitors da classe Win32 \_ TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="81b6b-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="81b6b-107">Define a propriedade **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="81b6b-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b6b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81b6b-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="81b6b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81b6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b6b-110">*MaxMonitors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81b6b-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81b6b-111">Especifica o novo número máximo de monitores com suporte no servidor.</span><span class="sxs-lookup"><span data-stu-id="81b6b-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="81b6b-112">O valor mínimo é 1 e o valor máximo é 10.</span><span class="sxs-lookup"><span data-stu-id="81b6b-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b6b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81b6b-113">Return value</span></span>

<span data-ttu-id="81b6b-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="81b6b-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="81b6b-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="81b6b-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="81b6b-116">O método retornará um erro se as configurações de conexão do usuário forem substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="81b6b-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b6b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b6b-117">Requirements</span></span>



| <span data-ttu-id="81b6b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b6b-118">Requirement</span></span> | <span data-ttu-id="81b6b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="81b6b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81b6b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81b6b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81b6b-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="81b6b-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="81b6b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81b6b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81b6b-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81b6b-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="81b6b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="81b6b-124">Namespace</span></span><br/>                | <span data-ttu-id="81b6b-125">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="81b6b-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="81b6b-126">MOF</span><span class="sxs-lookup"><span data-stu-id="81b6b-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81b6b-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81b6b-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="81b6b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="81b6b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81b6b-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b6b-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81b6b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="81b6b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b6b-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="81b6b-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





