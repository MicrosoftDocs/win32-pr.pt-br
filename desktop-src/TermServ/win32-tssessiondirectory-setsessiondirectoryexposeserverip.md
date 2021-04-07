---
title: Método SetSessionDirectoryExposeServerIP da classe Win32_TSSessionDirectory
description: Define a propriedade SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSessionDirectoryExposeServerIP
- Método SetSessionDirectoryExposeServerIP Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918303"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e9376-106">Método SetSessionDirectoryExposeServerIP da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="e9376-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e9376-107">Define a propriedade **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="e9376-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9376-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9376-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="e9376-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9376-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9376-110">*SessionDirectoryExposeServerIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9376-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9376-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9376-111">Type: **uint32**</span></span>

<span data-ttu-id="e9376-112">Sinalizador desabilitando ou habilitando a propriedade **SessionDirectoryExposeServerIP** que permite ou nega a recuperação do endereço IP para o diretório de sessão.</span><span class="sxs-lookup"><span data-stu-id="e9376-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e9376-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="e9376-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e9376-114">Desabilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9376-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="e9376-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e9376-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e9376-116">Habilite a propriedade.</span><span class="sxs-lookup"><span data-stu-id="e9376-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9376-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9376-117">Return value</span></span>

<span data-ttu-id="e9376-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9376-118">Type: **uint32**</span></span>

<span data-ttu-id="e9376-119">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="e9376-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e9376-120">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="e9376-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="e9376-121">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e9376-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9376-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9376-122">Remarks</span></span>

<span data-ttu-id="e9376-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e9376-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9376-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e9376-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9376-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e9376-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9376-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e9376-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9376-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9376-127">Requirements</span></span>



| <span data-ttu-id="e9376-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9376-128">Requirement</span></span> | <span data-ttu-id="e9376-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e9376-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9376-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9376-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e9376-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e9376-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e9376-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9376-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e9376-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9376-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9376-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9376-134">Namespace</span></span><br/>                | <span data-ttu-id="e9376-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e9376-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e9376-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e9376-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9376-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9376-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9376-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e9376-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9376-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9376-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9376-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9376-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9376-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="e9376-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

