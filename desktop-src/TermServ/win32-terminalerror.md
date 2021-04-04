---
title: Classe Win32_TerminalError
description: Representa um erro de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalError Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalError classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085296"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="e9529-105">\_Classe Win32 TerminalError</span><span class="sxs-lookup"><span data-stu-id="e9529-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="e9529-106">Representa um erro de terminal.</span><span class="sxs-lookup"><span data-stu-id="e9529-106">Represents a terminal error.</span></span>

<span data-ttu-id="e9529-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e9529-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9529-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9529-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="e9529-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e9529-109">Members</span></span>

<span data-ttu-id="e9529-110">A classe **Win32 \_ TerminalError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e9529-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="e9529-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9529-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9529-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9529-112">Properties</span></span>

<span data-ttu-id="e9529-113">A classe **Win32 \_ TerminalError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e9529-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9529-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9529-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9529-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-117">Qualquer cadeia de caracteres definida pelo usuário que descreva um erro ou status operacional.</span><span class="sxs-lookup"><span data-stu-id="e9529-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="e9529-118">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="e9529-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-119">**Operação**</span><span class="sxs-lookup"><span data-stu-id="e9529-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9529-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-122">Operação que ocorre no momento de uma falha ou anomalia.</span><span class="sxs-lookup"><span data-stu-id="e9529-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="e9529-123">Normalmente, o WMI define essa propriedade como o nome de uma API COM para o método WMI, como o seguinte: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="e9529-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="e9529-124">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="e9529-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="e9529-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9529-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-128">Parâmetros envolvidos em um erro ou alteração de status.</span><span class="sxs-lookup"><span data-stu-id="e9529-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="e9529-129">Por exemplo, se um aplicativo tentar recuperar uma classe que não existe, essa propriedade será definida como o nome da classe incorreta.</span><span class="sxs-lookup"><span data-stu-id="e9529-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="e9529-130">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="e9529-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="e9529-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9529-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-134">Identifica o provedor que causa ou relata um erro ou uma alteração de status.</span><span class="sxs-lookup"><span data-stu-id="e9529-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="e9529-135">Se um provedor não estiver envolvido, essa cadeia de caracteres será definida como "Gerenciamento do Windows".</span><span class="sxs-lookup"><span data-stu-id="e9529-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="e9529-136">Essa propriedade é herdada de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="e9529-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="e9529-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9529-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-140">Contém um código de erro ou informações para uma operação.</span><span class="sxs-lookup"><span data-stu-id="e9529-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="e9529-141">Pode ser qualquer valor definido pelo provedor, mas o valor 0 (zero) geralmente é reservado para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="e9529-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="e9529-142">Essa propriedade é herdada de [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span><span class="sxs-lookup"><span data-stu-id="e9529-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="e9529-143">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="e9529-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9529-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9529-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9529-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9529-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9529-146">O nome do Sin de terminal em que o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e9529-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9529-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9529-147">Requirements</span></span>



| <span data-ttu-id="e9529-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9529-148">Requirement</span></span> | <span data-ttu-id="e9529-149">Valor</span><span class="sxs-lookup"><span data-stu-id="e9529-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9529-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9529-150">Minimum supported client</span></span><br/> | <span data-ttu-id="e9529-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9529-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9529-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9529-152">Minimum supported server</span></span><br/> | <span data-ttu-id="e9529-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9529-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9529-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9529-154">Namespace</span></span><br/>                | <span data-ttu-id="e9529-155">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e9529-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e9529-156">MOF</span><span class="sxs-lookup"><span data-stu-id="e9529-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9529-157"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9529-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9529-158">DLL</span><span class="sxs-lookup"><span data-stu-id="e9529-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9529-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9529-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9529-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9529-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9529-161">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="e9529-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

