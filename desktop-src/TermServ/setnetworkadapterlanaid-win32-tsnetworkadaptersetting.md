---
title: Método SetNetworkAdapterLanaID da classe Win32_TSNetworkAdapterSetting
description: Especifica o número do adaptador de rede de área local (LANA) do adaptador de rede a ser definido.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetNetworkAdapterLanaID
- Método SetNetworkAdapterLanaID Serviços de Área de Trabalho Remota, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota, método SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645148"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="a0af9-106">Método SetNetworkAdapterLanaID da classe Win32 \_ TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="a0af9-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="a0af9-107">O método **SetNetworkAdapterLanaID** especifica o número do adaptador de rede de área local (Lana) do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="a0af9-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="a0af9-108">Se a ID de LANA especificada não for válida ou não existir, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="a0af9-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="a0af9-109">A lista de IDs de LANA disponíveis é obtida pela enumeração da propriedade **DeviceIDList** na classe [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a0af9-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0af9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0af9-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="a0af9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0af9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0af9-112">*NetworkAdapterLanaID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0af9-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0af9-113">Número da LANA do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="a0af9-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0af9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0af9-114">Return value</span></span>

<span data-ttu-id="a0af9-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a0af9-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a0af9-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a0af9-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0af9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0af9-117">Remarks</span></span>

<span data-ttu-id="a0af9-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a0af9-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a0af9-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a0af9-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a0af9-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a0af9-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a0af9-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a0af9-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0af9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0af9-122">Requirements</span></span>



| <span data-ttu-id="a0af9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0af9-123">Requirement</span></span> | <span data-ttu-id="a0af9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a0af9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0af9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0af9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a0af9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0af9-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0af9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0af9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a0af9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0af9-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0af9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0af9-129">Namespace</span></span><br/>                | <span data-ttu-id="a0af9-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a0af9-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a0af9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a0af9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0af9-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0af9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a0af9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0af9-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0af9-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0af9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0af9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0af9-136">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a0af9-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

