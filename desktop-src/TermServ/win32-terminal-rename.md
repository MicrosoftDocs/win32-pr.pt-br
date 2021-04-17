---
title: Método Rename da classe Win32_Terminal
description: O método renomear renomeia o terminal.
ms.assetid: 85b5c83b-8ca3-4ed0-852b-b11ba98c18a6
ms.tgt_platform: multiple
keywords:
- Renomear o método Serviços de Área de Trabalho Remota
- Método Rename Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Rename
topic_type:
- apiref
api_name:
- Win32_Terminal.Rename
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0258277bd509f7f72d5e314bc20d9852fa03315a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769375"
---
# <a name="rename-method-of-the-win32_terminal-class"></a><span data-ttu-id="c46e4-106">Método Rename da \_ classe terminal do Win32</span><span class="sxs-lookup"><span data-stu-id="c46e4-106">Rename method of the Win32\_Terminal class</span></span>

<span data-ttu-id="c46e4-107">O método **renomear** renomeia o terminal.</span><span class="sxs-lookup"><span data-stu-id="c46e4-107">The **Rename** method renames the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46e4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c46e4-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="c46e4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c46e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c46e4-110">*NewTerminalName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c46e4-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46e4-111">O novo nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="c46e4-111">The new name of the terminal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c46e4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c46e4-112">Return value</span></span>

<span data-ttu-id="c46e4-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="c46e4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c46e4-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="c46e4-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c46e4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c46e4-115">Remarks</span></span>

<span data-ttu-id="c46e4-116">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c46e4-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c46e4-117">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c46e4-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c46e4-118">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c46e4-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c46e4-119">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c46e4-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c46e4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c46e4-120">Requirements</span></span>



| <span data-ttu-id="c46e4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c46e4-121">Requirement</span></span> | <span data-ttu-id="c46e4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c46e4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c46e4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c46e4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c46e4-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c46e4-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c46e4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c46e4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c46e4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c46e4-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c46e4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c46e4-127">Namespace</span></span><br/>                | <span data-ttu-id="c46e4-128">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c46e4-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c46e4-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c46e4-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c46e4-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c46e4-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c46e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c46e4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c46e4-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c46e4-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46e4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c46e4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46e4-134">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c46e4-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

