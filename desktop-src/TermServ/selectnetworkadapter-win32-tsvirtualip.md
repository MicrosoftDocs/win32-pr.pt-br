---
title: Método SelectNetworkAdapter da classe Win32_TSVirtualIP
description: Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SelectNetworkAdapter
- Método SelectNetworkAdapter Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918367"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="a92e4-106">Método SelectNetworkAdapter da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a92e4-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="a92e4-107">Define o endereço MAC do adaptador de rede a ser usado para virtualização de IP.</span><span class="sxs-lookup"><span data-stu-id="a92e4-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92e4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a92e4-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="a92e4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a92e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92e4-110">*NetworkAdapterMacAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a92e4-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a92e4-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a92e4-111">Type: **string**</span></span>

<span data-ttu-id="a92e4-112">Especifica o endereço MAC do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="a92e4-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92e4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a92e4-113">Return value</span></span>

<span data-ttu-id="a92e4-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a92e4-114">Type: **uint32**</span></span>

<span data-ttu-id="a92e4-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a92e4-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a92e4-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a92e4-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="a92e4-117">Se o endereço MAC for inválido ou não existir, ou se o modo de virtualização de IP for por sessão, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="a92e4-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="a92e4-118">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a92e4-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92e4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a92e4-119">Requirements</span></span>



| <span data-ttu-id="a92e4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a92e4-120">Requirement</span></span> | <span data-ttu-id="a92e4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a92e4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a92e4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a92e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a92e4-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a92e4-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a92e4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a92e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a92e4-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a92e4-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a92e4-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a92e4-126">Namespace</span></span><br/>                | <span data-ttu-id="a92e4-127">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a92e4-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a92e4-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a92e4-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a92e4-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a92e4-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a92e4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a92e4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a92e4-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a92e4-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a92e4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a92e4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92e4-133">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="a92e4-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





