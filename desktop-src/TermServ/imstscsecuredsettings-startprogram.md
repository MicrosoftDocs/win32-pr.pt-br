---
title: Propriedade IMsTscSecuredSettings StartProgram
description: Especifica o programa a ser iniciado no servidor remoto durante a conexão.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade StartProgram
- Propriedade StartProgram Serviços de Área de Trabalho Remota, interface IMsTscSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsTscSecuredSettings, Propriedade StartProgram
- Propriedade StartProgram Serviços de Área de Trabalho Remota, interface IMsRdpClientSecuredSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientSecuredSettings, Propriedade StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796298"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="0dad1-108">Propriedade IMsTscSecuredSettings:: StartProgram</span><span class="sxs-lookup"><span data-stu-id="0dad1-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="0dad1-109">Especifica o programa a ser iniciado no servidor remoto durante a conexão.</span><span class="sxs-lookup"><span data-stu-id="0dad1-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="0dad1-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0dad1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dad1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dad1-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="0dad1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0dad1-112">Property value</span></span>

<span data-ttu-id="0dad1-113">O nome do novo programa de início.</span><span class="sxs-lookup"><span data-stu-id="0dad1-113">The name of the new start program.</span></span> <span data-ttu-id="0dad1-114">O comprimento máximo dessa cadeia de caracteres é o **\_ caminho máximo**-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0dad1-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0dad1-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0dad1-115">Error codes</span></span>

<span data-ttu-id="0dad1-116">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0dad1-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dad1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dad1-117">Remarks</span></span>

<span data-ttu-id="0dad1-118">Se o valor dessa propriedade não for definido, o comando do shell do usuário da sessão será executado.</span><span class="sxs-lookup"><span data-stu-id="0dad1-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="0dad1-119">O comando do shell será lido a partir do seguinte valor do registro no servidor:</span><span class="sxs-lookup"><span data-stu-id="0dad1-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="0dad1-120">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **shell**</span><span class="sxs-lookup"><span data-stu-id="0dad1-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="0dad1-121">Consulte [fornecer para o RDP Client Security](providing-for-rdp-client-security.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0dad1-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="0dad1-122">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0dad1-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dad1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dad1-123">Requirements</span></span>



| <span data-ttu-id="0dad1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dad1-124">Requirement</span></span> | <span data-ttu-id="0dad1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0dad1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dad1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dad1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dad1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dad1-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0dad1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dad1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dad1-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dad1-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0dad1-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0dad1-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="0dad1-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0dad1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0dad1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dad1-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0dad1-134">IID</span><span class="sxs-lookup"><span data-stu-id="0dad1-134">IID</span></span><br/>                      | <span data-ttu-id="0dad1-135">IID \_ IMsTscSecuredSettings é definido como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="0dad1-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0dad1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0dad1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dad1-137">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="0dad1-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0dad1-138">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="0dad1-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





