---
title: Método CreateWinstation da classe Win32_TerminalServiceSetting
description: Cria uma nova pilha de ouvinte com base na combinação exclusiva de nome do ouvinte e NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateWinstation
- Método CreateWinstation Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779432"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="35dbd-106">Método CreateWinstation da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="35dbd-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="35dbd-107">O método **CreateWinstation** cria uma nova pilha de ouvinte com base na combinação exclusiva de nome do ouvinte e NIC.</span><span class="sxs-lookup"><span data-stu-id="35dbd-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dbd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35dbd-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="35dbd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35dbd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35dbd-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="35dbd-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dbd-111">Nome do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="35dbd-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="35dbd-112">*WinstaDriverName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35dbd-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dbd-113">O nome do driver WinStation.</span><span class="sxs-lookup"><span data-stu-id="35dbd-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="35dbd-114">*Lanaid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="35dbd-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dbd-115">Número de adaptador de rede de área local (LANA) do NetBIOS para a NIC.</span><span class="sxs-lookup"><span data-stu-id="35dbd-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35dbd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35dbd-116">Return value</span></span>

<span data-ttu-id="35dbd-117">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="35dbd-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="35dbd-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="35dbd-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="35dbd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="35dbd-119">Remarks</span></span>

<span data-ttu-id="35dbd-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35dbd-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35dbd-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="35dbd-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35dbd-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="35dbd-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35dbd-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35dbd-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35dbd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35dbd-124">Requirements</span></span>



| <span data-ttu-id="35dbd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dbd-125">Requirement</span></span> | <span data-ttu-id="35dbd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="35dbd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35dbd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35dbd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35dbd-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35dbd-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35dbd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35dbd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35dbd-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35dbd-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35dbd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="35dbd-131">Namespace</span></span><br/>                | <span data-ttu-id="35dbd-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="35dbd-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="35dbd-133">MOF</span><span class="sxs-lookup"><span data-stu-id="35dbd-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35dbd-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35dbd-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="35dbd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="35dbd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35dbd-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35dbd-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dbd-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="35dbd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dbd-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="35dbd-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

