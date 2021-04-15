---
title: Método SelectNetworkAdapterIP da classe Win32_TSNetworkAdapterSetting
description: Seleciona um adaptador de rede com base no endereço IP do adaptador.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectNetworkAdapterIP
- Método SelectNetworkAdapterIP Serviços de Área de Trabalho Remota, classe Win32_TSNetworkAdapterSetting
- Classe Win32_TSNetworkAdapterSetting Serviços de Área de Trabalho Remota, método SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761321"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="31a69-106">Método SelectNetworkAdapterIP da classe Win32 \_ TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="31a69-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="31a69-107">Seleciona um adaptador de rede com base no endereço IP do adaptador.</span><span class="sxs-lookup"><span data-stu-id="31a69-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a69-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31a69-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="31a69-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31a69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a69-110">*NetworkAdapterIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31a69-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a69-111">O endereço IP do adaptador de rede a ser definido.</span><span class="sxs-lookup"><span data-stu-id="31a69-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a69-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31a69-112">Return value</span></span>

<span data-ttu-id="31a69-113">Retornará zero se o endereço IP especificado for válido e retornar um código de erro WMI se o endereço IP for inválido ou não existir.</span><span class="sxs-lookup"><span data-stu-id="31a69-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="31a69-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="31a69-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a69-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="31a69-115">Remarks</span></span>

<span data-ttu-id="31a69-116">Você pode recuperar o endereço IP de um adaptador de rede enumerando as propriedades da classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="31a69-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="31a69-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="31a69-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="31a69-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="31a69-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="31a69-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="31a69-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="31a69-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="31a69-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="31a69-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a69-121">Requirements</span></span>



| <span data-ttu-id="31a69-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a69-122">Requirement</span></span> | <span data-ttu-id="31a69-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31a69-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31a69-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31a69-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31a69-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31a69-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31a69-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31a69-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31a69-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31a69-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31a69-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="31a69-128">Namespace</span></span><br/>                | <span data-ttu-id="31a69-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="31a69-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="31a69-130">MOF</span><span class="sxs-lookup"><span data-stu-id="31a69-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31a69-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31a69-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="31a69-132">DLL</span><span class="sxs-lookup"><span data-stu-id="31a69-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a69-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a69-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a69-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="31a69-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a69-135">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="31a69-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

