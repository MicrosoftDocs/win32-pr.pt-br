---
description: Método Shell. GetSystemInformation – recupera informações do sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Método Shell. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104274"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="b1f65-103">Método Shell. GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="b1f65-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="b1f65-104">Recupera informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1f65-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1f65-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="b1f65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1f65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1f65-107">*sname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1f65-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1f65-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b1f65-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b1f65-109">Uma **cadeia de caracteres** que especifica as informações do sistema que estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b1f65-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1f65-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1f65-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b1f65-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b1f65-111">JScript</span></span>

<span data-ttu-id="b1f65-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="b1f65-112">Type: **Variant**</span></span>

<span data-ttu-id="b1f65-113">Retorna o valor das informações do sistema solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b1f65-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="b1f65-114">O tipo de retorno depende de quais informações do sistema são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b1f65-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="b1f65-115">Consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1f65-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="b1f65-116">VB</span><span class="sxs-lookup"><span data-stu-id="b1f65-116">VB</span></span>

<span data-ttu-id="b1f65-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="b1f65-117">Type: **Variant**</span></span>

<span data-ttu-id="b1f65-118">Retorna o valor das informações do sistema solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b1f65-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="b1f65-119">O tipo de retorno depende de quais informações do sistema são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="b1f65-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="b1f65-120">Consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1f65-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f65-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1f65-121">Remarks</span></span>

<span data-ttu-id="b1f65-122">Esse método pode ser usado para solicitar muitos valores de informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1f65-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="b1f65-123">A tabela a seguir fornece o valor de *sname* que é usado para solicitar as informações e o tipo associado do valor retornado.</span><span class="sxs-lookup"><span data-stu-id="b1f65-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="b1f65-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="b1f65-124">*sName*</span></span>

<span data-ttu-id="b1f65-125">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="b1f65-125">Return type</span></span>

<span data-ttu-id="b1f65-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1f65-126">Description</span></span>

<span data-ttu-id="b1f65-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="b1f65-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="b1f65-128">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="b1f65-128">**Boolean**</span></span>

<span data-ttu-id="b1f65-129">Defina como **true** se o serviço de diretório estiver disponível; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b1f65-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="b1f65-130">DoubleClicktime</span><span class="sxs-lookup"><span data-stu-id="b1f65-130">DoubleClickTime</span></span>

<span data-ttu-id="b1f65-131">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="b1f65-131">**Integer**</span></span>

<span data-ttu-id="b1f65-132">O tempo de clique duplo, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b1f65-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="b1f65-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="b1f65-133">ProcessorLevel</span></span>

<span data-ttu-id="b1f65-134">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="b1f65-134">**Integer**</span></span>

<span data-ttu-id="b1f65-135">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="b1f65-135">**Windows Vista and later**.</span></span> <span data-ttu-id="b1f65-136">O nível do processador.</span><span class="sxs-lookup"><span data-stu-id="b1f65-136">The processor level.</span></span> <span data-ttu-id="b1f65-137">Retorna 3, 4 ou 5, para os processadores de nível X386, x486 e Pentium, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b1f65-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="b1f65-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="b1f65-138">ProcessorSpeed</span></span>

<span data-ttu-id="b1f65-139">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="b1f65-139">**Integer**</span></span>

<span data-ttu-id="b1f65-140">A velocidade do processador, em megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="b1f65-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="b1f65-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="b1f65-141">ProcessorArchitecture</span></span>

<span data-ttu-id="b1f65-142">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="b1f65-142">**Integer**</span></span>

<span data-ttu-id="b1f65-143">A arquitetura do processador.</span><span class="sxs-lookup"><span data-stu-id="b1f65-143">The processor architecture.</span></span> <span data-ttu-id="b1f65-144">Para obter detalhes, consulte a discussão do membro **wProcessorArchitecture** da estrutura [**de \_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="b1f65-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="b1f65-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="b1f65-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="b1f65-146">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="b1f65-146">**Integer**</span></span>

<span data-ttu-id="b1f65-147">A quantidade de memória física instalada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b1f65-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="b1f65-148">Os itens a seguir são válidos somente no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b1f65-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="b1f65-149">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="b1f65-149">IsOS\_Professional</span></span>

<span data-ttu-id="b1f65-150">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="b1f65-150">**Boolean**</span></span>

<span data-ttu-id="b1f65-151">Defina como **true** se o sistema operacional for o Windows XP Professional Edition; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b1f65-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="b1f65-152">IsOS \_ pessoal</span><span class="sxs-lookup"><span data-stu-id="b1f65-152">IsOS\_Personal</span></span>

<span data-ttu-id="b1f65-153">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="b1f65-153">**Boolean**</span></span>

<span data-ttu-id="b1f65-154">Defina como **true** se o sistema operacional for o Windows XP Home Edition; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b1f65-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="b1f65-155">O seguinte é válido somente no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="b1f65-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="b1f65-156">IsOS \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="b1f65-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="b1f65-157">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="b1f65-157">**Boolean**</span></span>

<span data-ttu-id="b1f65-158">Defina como **true** se o computador for membro de um domínio; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b1f65-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="b1f65-159">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b1f65-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b1f65-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1f65-160">Examples</span></span>

<span data-ttu-id="b1f65-161">Os exemplos a seguir mostram o uso de **GetSystemInformation** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="b1f65-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="b1f65-162">JScript</span><span class="sxs-lookup"><span data-stu-id="b1f65-162">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="b1f65-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="b1f65-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="b1f65-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f65-164">Requirements</span></span>



| <span data-ttu-id="b1f65-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f65-165">Requirement</span></span> | <span data-ttu-id="b1f65-166">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f65-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f65-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f65-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f65-168">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1f65-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1f65-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1f65-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f65-170">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1f65-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b1f65-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1f65-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f65-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f65-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b1f65-173">INSERI</span><span class="sxs-lookup"><span data-stu-id="b1f65-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1f65-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1f65-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b1f65-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b1f65-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f65-176"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b1f65-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
