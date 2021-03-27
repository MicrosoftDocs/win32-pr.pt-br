---
description: Recupera informações do sistema.
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Método IShellDispatch2. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 624c7383d458f20a13f0e2249ec302181fc4a7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827399"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="f9b53-103">Método IShellDispatch2. GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="f9b53-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="f9b53-104">Recupera informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9b53-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9b53-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="f9b53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9b53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9b53-107">*sname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9b53-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9b53-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="f9b53-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="f9b53-109">Uma **cadeia de caracteres** que especifica as informações do sistema que estão sendo solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f9b53-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9b53-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9b53-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f9b53-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f9b53-111">JScript</span></span>

<span data-ttu-id="f9b53-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f9b53-112">Type: **Variant**</span></span>

<span data-ttu-id="f9b53-113">Retorna o valor das informações do sistema solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f9b53-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="f9b53-114">O tipo de retorno depende de quais informações do sistema são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f9b53-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="f9b53-115">Consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="f9b53-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="f9b53-116">VB</span><span class="sxs-lookup"><span data-stu-id="f9b53-116">VB</span></span>

<span data-ttu-id="f9b53-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f9b53-117">Type: **Variant**</span></span>

<span data-ttu-id="f9b53-118">Retorna o valor das informações do sistema solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f9b53-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="f9b53-119">O tipo de retorno depende de quais informações do sistema são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f9b53-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="f9b53-120">Consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="f9b53-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9b53-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9b53-121">Remarks</span></span>

<span data-ttu-id="f9b53-122">Esse método é implementado e acessado por meio do método [**shell. GetSystemInformation**](./shell-getsysteminformation.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b53-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="f9b53-123">Esse método pode ser usado para solicitar muitos valores de informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="f9b53-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="f9b53-124">A tabela a seguir fornece o valor de *sname* que é usado para solicitar as informações e o tipo associado do valor retornado.</span><span class="sxs-lookup"><span data-stu-id="f9b53-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="f9b53-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="f9b53-125">*sName*</span></span>

<span data-ttu-id="f9b53-126">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="f9b53-126">Return type</span></span>

<span data-ttu-id="f9b53-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9b53-127">Description</span></span>

<span data-ttu-id="f9b53-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="f9b53-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="f9b53-129">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="f9b53-129">**Boolean**</span></span>

<span data-ttu-id="f9b53-130">Defina como **true** se o serviço de diretório estiver disponível; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f9b53-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="f9b53-131">DoubleClicktime</span><span class="sxs-lookup"><span data-stu-id="f9b53-131">DoubleClickTime</span></span>

<span data-ttu-id="f9b53-132">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9b53-132">**Integer**</span></span>

<span data-ttu-id="f9b53-133">O tempo de clique duplo, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="f9b53-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="f9b53-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="f9b53-134">ProcessorLevel</span></span>

<span data-ttu-id="f9b53-135">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9b53-135">**Integer**</span></span>

<span data-ttu-id="f9b53-136">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="f9b53-136">**Windows Vista and later**.</span></span> <span data-ttu-id="f9b53-137">O nível do processador.</span><span class="sxs-lookup"><span data-stu-id="f9b53-137">The processor level.</span></span> <span data-ttu-id="f9b53-138">Retorna 3, 4 ou 5, para os processadores de nível X386, x486 e Pentium, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f9b53-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="f9b53-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="f9b53-139">ProcessorSpeed</span></span>

<span data-ttu-id="f9b53-140">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9b53-140">**Integer**</span></span>

<span data-ttu-id="f9b53-141">A velocidade do processador, em megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="f9b53-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="f9b53-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f9b53-142">ProcessorArchitecture</span></span>

<span data-ttu-id="f9b53-143">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9b53-143">**Integer**</span></span>

<span data-ttu-id="f9b53-144">A arquitetura do processador.</span><span class="sxs-lookup"><span data-stu-id="f9b53-144">The processor architecture.</span></span> <span data-ttu-id="f9b53-145">Para obter detalhes, consulte a discussão do membro **wProcessorArchitecture** da estrutura [**de \_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="f9b53-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="f9b53-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="f9b53-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="f9b53-147">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9b53-147">**Integer**</span></span>

<span data-ttu-id="f9b53-148">A quantidade de memória física instalada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f9b53-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="f9b53-149">Os itens a seguir são válidos somente no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9b53-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="f9b53-150">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="f9b53-150">IsOS\_Professional</span></span>

<span data-ttu-id="f9b53-151">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="f9b53-151">**Boolean**</span></span>

<span data-ttu-id="f9b53-152">Defina como **true** se o sistema operacional for o Windows XP Professional Edition; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f9b53-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="f9b53-153">IsOS \_ pessoal</span><span class="sxs-lookup"><span data-stu-id="f9b53-153">IsOS\_Personal</span></span>

<span data-ttu-id="f9b53-154">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="f9b53-154">**Boolean**</span></span>

<span data-ttu-id="f9b53-155">Defina como **true** se o sistema operacional for o Windows XP Home Edition; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f9b53-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="f9b53-156">O seguinte é válido somente no Windows XP e posterior.</span><span class="sxs-lookup"><span data-stu-id="f9b53-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="f9b53-157">IsOS \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="f9b53-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="f9b53-158">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="f9b53-158">**Boolean**</span></span>

<span data-ttu-id="f9b53-159">Defina como **true** se o computador for membro de um domínio; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f9b53-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="f9b53-160">Este método não está disponível atualmente no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f9b53-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="f9b53-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9b53-161">Examples</span></span>

<span data-ttu-id="f9b53-162">Os exemplos a seguir mostram o uso de **GetSystemInformation** para JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="f9b53-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="f9b53-163">JScript</span><span class="sxs-lookup"><span data-stu-id="f9b53-163">JScript:</span></span>


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



<span data-ttu-id="f9b53-164">VBScript</span><span class="sxs-lookup"><span data-stu-id="f9b53-164">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f9b53-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9b53-165">Requirements</span></span>



| <span data-ttu-id="f9b53-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b53-166">Requirement</span></span> | <span data-ttu-id="f9b53-167">Valor</span><span class="sxs-lookup"><span data-stu-id="f9b53-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b53-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9b53-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f9b53-169">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9b53-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9b53-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9b53-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f9b53-171">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9b53-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f9b53-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9b53-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9b53-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b53-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f9b53-174">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9b53-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9b53-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9b53-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f9b53-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f9b53-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9b53-177"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f9b53-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
