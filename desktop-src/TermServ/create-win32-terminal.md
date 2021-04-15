---
title: Método Create da classe Win32_Terminal
description: Cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e métodos das \_ classes TerminalSetting do Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454788"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="d8b38-106">Método Create da \_ classe terminal do Win32</span><span class="sxs-lookup"><span data-stu-id="d8b38-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="d8b38-107">O método **Create** cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e métodos das classes [**\_ TerminalSetting do Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b38-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="d8b38-108">A função retorna zero em caso de êxito e um erro na falha.</span><span class="sxs-lookup"><span data-stu-id="d8b38-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b38-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8b38-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="d8b38-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8b38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b38-111">*NewTerminalName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8b38-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b38-112">Nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="d8b38-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="d8b38-113">*Transporte* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8b38-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b38-114">Transporte para o terminal.</span><span class="sxs-lookup"><span data-stu-id="d8b38-114">Transport for the terminal.</span></span> <span data-ttu-id="d8b38-115">Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b38-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d8b38-116">*TerminalProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8b38-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b38-117">Protocolo para o terminal.</span><span class="sxs-lookup"><span data-stu-id="d8b38-117">Protocol for the terminal.</span></span> <span data-ttu-id="d8b38-118">Essa é uma propriedade da classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b38-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b38-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8b38-119">Return value</span></span>

<span data-ttu-id="d8b38-120">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d8b38-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d8b38-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="d8b38-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b38-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8b38-122">Remarks</span></span>

<span data-ttu-id="d8b38-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d8b38-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d8b38-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d8b38-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d8b38-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d8b38-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d8b38-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d8b38-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b38-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8b38-127">Requirements</span></span>



| <span data-ttu-id="d8b38-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b38-128">Requirement</span></span> | <span data-ttu-id="d8b38-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d8b38-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b38-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b38-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8b38-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8b38-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8b38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b38-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8b38-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8b38-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8b38-134">Namespace</span></span><br/>                | <span data-ttu-id="d8b38-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d8b38-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d8b38-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d8b38-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8b38-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8b38-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8b38-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b38-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b38-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8b38-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b38-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8b38-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b38-141">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d8b38-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

