---
title: Método BrokenConnection da classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Define a propriedade BrokenConnectionAction, que é a ação que o servidor executará se o limite de tempo de sessão for atingido ou se a conexão for interrompida.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método BrokenConnection
- Método BrokenConnection Serviços de Área de Trabalho Remota, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Serviços de Área de Trabalho Remota, método BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788022"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="773b7-106">Método BrokenConnection da classe Win32 \_ TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="773b7-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="773b7-107">Define a propriedade **BrokenConnectionAction** , que é a ação que o servidor executará se o limite de tempo de sessão for atingido ou se a conexão for interrompida.</span><span class="sxs-lookup"><span data-stu-id="773b7-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="773b7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="773b7-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="773b7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="773b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773b7-110">*BrokenConnectionAction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="773b7-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773b7-111">A ação a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="773b7-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="773b7-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)</span><span class="sxs-lookup"><span data-stu-id="773b7-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="773b7-113">O usuário está desconectado da sessão.</span><span class="sxs-lookup"><span data-stu-id="773b7-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="773b7-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (1)</span><span class="sxs-lookup"><span data-stu-id="773b7-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="773b7-115">A sessão é excluída permanentemente do servidor.</span><span class="sxs-lookup"><span data-stu-id="773b7-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773b7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="773b7-116">Return value</span></span>

<span data-ttu-id="773b7-117">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="773b7-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="773b7-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="773b7-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="773b7-119">O método retornará um erro se a configuração estiver sob Política de Grupo controle.</span><span class="sxs-lookup"><span data-stu-id="773b7-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="773b7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="773b7-120">Remarks</span></span>

<span data-ttu-id="773b7-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="773b7-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="773b7-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="773b7-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="773b7-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="773b7-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="773b7-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="773b7-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="773b7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="773b7-125">Requirements</span></span>



| <span data-ttu-id="773b7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="773b7-126">Requirement</span></span> | <span data-ttu-id="773b7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="773b7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="773b7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="773b7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="773b7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="773b7-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="773b7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="773b7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="773b7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="773b7-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="773b7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="773b7-132">Namespace</span></span><br/>                | <span data-ttu-id="773b7-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="773b7-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="773b7-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="773b7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="773b7-135"><dt>Wtsprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="773b7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="773b7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="773b7-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="773b7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="773b7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="773b7-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="773b7-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="773b7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="773b7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773b7-141">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="773b7-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

