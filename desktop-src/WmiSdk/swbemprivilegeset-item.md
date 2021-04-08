---
description: O método item do objeto SWbemPrivilegeSet retorna um objeto SWbemPrivilege da coleção. O método item é o método padrão de um objeto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827713"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="679d7-104">Método SWbemPrivilegeSet. Item</span><span class="sxs-lookup"><span data-stu-id="679d7-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="679d7-105">O método **Item** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) retorna um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="679d7-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="679d7-106">O método **Item** é o método padrão de um objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="679d7-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="679d7-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="679d7-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="679d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="679d7-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="679d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="679d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679d7-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="679d7-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="679d7-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="679d7-111">Required.</span></span> <span data-ttu-id="679d7-112">Uma das constantes do WMI do grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="679d7-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="679d7-113">Essas constantes são essencialmente inteiros que representam privilégios específicos.</span><span class="sxs-lookup"><span data-stu-id="679d7-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="679d7-114">Por exemplo, para obter o privilégio que permite que você desligue um sistema Windows, use a constante **wbemPrivilegeShutdown** ou o equivalente numérico de 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="679d7-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="679d7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="679d7-115">Return value</span></span>

<span data-ttu-id="679d7-116">Se for bem-sucedido, o objeto [**SWbemPrivilege**](swbemprivilege.md) solicitado será retornado.</span><span class="sxs-lookup"><span data-stu-id="679d7-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="679d7-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="679d7-117">Error codes</span></span>

<span data-ttu-id="679d7-118">Após a conclusão do método **Item** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="679d7-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="679d7-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="679d7-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="679d7-120">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="679d7-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="679d7-121">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="679d7-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="679d7-122">O privilégio especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="679d7-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="679d7-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="679d7-123">Examples</span></span>

<span data-ttu-id="679d7-124">O exemplo de código VBScript a seguir usa o método **Item**</span><span class="sxs-lookup"><span data-stu-id="679d7-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="679d7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="679d7-125">Requirements</span></span>



| <span data-ttu-id="679d7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="679d7-126">Requirement</span></span> | <span data-ttu-id="679d7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="679d7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="679d7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="679d7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="679d7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="679d7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="679d7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="679d7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="679d7-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="679d7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="679d7-133"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="679d7-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="679d7-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="679d7-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="679d7-135"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="679d7-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="679d7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="679d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="679d7-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="679d7-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="679d7-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="679d7-138">CLSID</span></span><br/>                    | <span data-ttu-id="679d7-139">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="679d7-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="679d7-140">IID</span><span class="sxs-lookup"><span data-stu-id="679d7-140">IID</span></span><br/>                      | <span data-ttu-id="679d7-141">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="679d7-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="679d7-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="679d7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679d7-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="679d7-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="679d7-144">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="679d7-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="679d7-145">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="679d7-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




