---
title: Método SetTSRedirectorMode da classe Win32_TSSessionDirectory
description: Define o valor para indicar se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetTSRedirectorMode
- Método SetTSRedirectorMode Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824730"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="8b899-106">Método SetTSRedirectorMode da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="8b899-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="8b899-107">Define o valor para indicar se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8b899-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b899-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b899-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="8b899-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b899-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b899-110">*TSRedirValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b899-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b899-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b899-111">Type: **uint32**</span></span>

<span data-ttu-id="8b899-112">Especifica se o servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8b899-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="8b899-113">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b899-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="8b899-114">0</span><span class="sxs-lookup"><span data-stu-id="8b899-114">0</span></span>
</dt> <dd>

<span data-ttu-id="8b899-115">O servidor atuará como um redirecionador Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8b899-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="8b899-116">1</span><span class="sxs-lookup"><span data-stu-id="8b899-116">1</span></span>
</dt> <dd>

<span data-ttu-id="8b899-117">O servidor não funcionará como um redirecionador de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8b899-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b899-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b899-118">Return value</span></span>

<span data-ttu-id="8b899-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b899-119">Type: **uint32**</span></span>

<span data-ttu-id="8b899-120">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="8b899-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="8b899-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="8b899-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="8b899-122">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="8b899-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b899-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b899-123">Remarks</span></span>

<span data-ttu-id="8b899-124">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8b899-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8b899-125">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8b899-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8b899-126">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8b899-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8b899-127">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8b899-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b899-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b899-128">Requirements</span></span>



| <span data-ttu-id="8b899-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b899-129">Requirement</span></span> | <span data-ttu-id="8b899-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8b899-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b899-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b899-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b899-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b899-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8b899-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b899-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b899-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b899-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8b899-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8b899-135">End of client support</span></span><br/>    | <span data-ttu-id="8b899-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b899-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8b899-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8b899-137">End of server support</span></span><br/>    | <span data-ttu-id="8b899-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b899-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="8b899-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b899-139">Namespace</span></span><br/>                | <span data-ttu-id="8b899-140">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8b899-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8b899-141">MOF</span><span class="sxs-lookup"><span data-stu-id="8b899-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b899-142"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b899-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b899-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8b899-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b899-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b899-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b899-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b899-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b899-146">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8b899-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

