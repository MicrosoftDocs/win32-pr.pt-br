---
title: Método SetServerWeight da classe Win32_TSSessionDirectory
description: Define o valor de peso do servidor para o balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetServerWeight
- Método SetServerWeight Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455479"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="8471c-106">Método SetServerWeight da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="8471c-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="8471c-107">Define o valor de peso do servidor para o balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="8471c-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8471c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8471c-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="8471c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8471c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8471c-110">*ServerWeightValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8471c-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8471c-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8471c-111">Type: **uint32**</span></span>

<span data-ttu-id="8471c-112">O valor de peso do servidor.</span><span class="sxs-lookup"><span data-stu-id="8471c-112">The server weight value.</span></span> <span data-ttu-id="8471c-113">O intervalo válido é de 1 a 10000.</span><span class="sxs-lookup"><span data-stu-id="8471c-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8471c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8471c-114">Remarks</span></span>

<span data-ttu-id="8471c-115">Por padrão, na interface do usuário da configuração do Serviços de Área de Trabalho Remota, o valor do peso do servidor é 100.</span><span class="sxs-lookup"><span data-stu-id="8471c-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="8471c-116">O peso do servidor é relativo.</span><span class="sxs-lookup"><span data-stu-id="8471c-116">The server weight is relative.</span></span> <span data-ttu-id="8471c-117">Portanto, se você atribuir a um servidor um valor de 100 e um valor de 200, o servidor com um peso relativo de 200 receberá o dobro do número de sessões.</span><span class="sxs-lookup"><span data-stu-id="8471c-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="8471c-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8471c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8471c-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8471c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8471c-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8471c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8471c-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8471c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8471c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8471c-122">Requirements</span></span>



| <span data-ttu-id="8471c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8471c-123">Requirement</span></span> | <span data-ttu-id="8471c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8471c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8471c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8471c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8471c-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8471c-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8471c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8471c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8471c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8471c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8471c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8471c-129">Namespace</span></span><br/>                | <span data-ttu-id="8471c-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8471c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8471c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8471c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8471c-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8471c-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8471c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8471c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8471c-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8471c-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8471c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8471c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8471c-136">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8471c-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

