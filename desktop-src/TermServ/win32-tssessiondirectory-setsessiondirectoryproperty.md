---
title: Método SetSessionDirectoryProperty da classe Win32_TSSessionDirectory
description: Define a propriedade SessionDirectoryLocation ou a propriedade SessionDirectoryClusterName para a classe.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSessionDirectoryProperty
- Método SetSessionDirectoryProperty Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454971"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="3004c-106">Método SetSessionDirectoryProperty da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="3004c-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="3004c-107">Define a propriedade **SessionDirectoryLocation** ou a propriedade **SessionDirectoryClusterName** para a classe.</span><span class="sxs-lookup"><span data-stu-id="3004c-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="3004c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3004c-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="3004c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3004c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3004c-110">*PropertyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3004c-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3004c-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3004c-111">Type: **string**</span></span>

<span data-ttu-id="3004c-112">Especifica a propriedade que o método está configurando.</span><span class="sxs-lookup"><span data-stu-id="3004c-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="3004c-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="3004c-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="3004c-114">O método está definindo a propriedade **SessionDirectoryLocation** .</span><span class="sxs-lookup"><span data-stu-id="3004c-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="3004c-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="3004c-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="3004c-116">O método está definindo a propriedade **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="3004c-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3004c-117">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3004c-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3004c-118">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3004c-118">Type: **string**</span></span>

<span data-ttu-id="3004c-119">O novo valor para a propriedade especificada pelo parâmetro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="3004c-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3004c-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3004c-120">Return value</span></span>

<span data-ttu-id="3004c-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3004c-121">Type: **uint32**</span></span>

<span data-ttu-id="3004c-122">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="3004c-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3004c-123">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="3004c-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="3004c-124">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3004c-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3004c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3004c-125">Remarks</span></span>

<span data-ttu-id="3004c-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3004c-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3004c-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3004c-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3004c-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="3004c-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3004c-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3004c-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3004c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3004c-130">Requirements</span></span>



| <span data-ttu-id="3004c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3004c-131">Requirement</span></span> | <span data-ttu-id="3004c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3004c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3004c-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3004c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3004c-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3004c-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3004c-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3004c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3004c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3004c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3004c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="3004c-137">Namespace</span></span><br/>                | <span data-ttu-id="3004c-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="3004c-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3004c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3004c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3004c-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3004c-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3004c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3004c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3004c-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3004c-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3004c-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="3004c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3004c-144">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="3004c-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

