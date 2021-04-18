---
description: Você pode usar o método AddAsString do objeto SWbemPrivilegeSet para adicionar um privilégio a uma coleção SWbemPrivilegeSet usando uma cadeia de caracteres de privilégio.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. AddAsString (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772988"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="631e2-103">Método SWbemPrivilegeSet. AddAsString</span><span class="sxs-lookup"><span data-stu-id="631e2-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="631e2-104">Você pode usar o método **AddAsString** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) para adicionar um privilégio a uma coleção **SWbemPrivilegeSet** usando uma cadeia de caracteres de privilégio.</span><span class="sxs-lookup"><span data-stu-id="631e2-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="631e2-105">Use este método para adicionar um privilégio ou para habilitar um privilégio para objetos [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="631e2-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="631e2-106">Consulte [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="631e2-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="631e2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="631e2-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="631e2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="631e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="631e2-110">*strPrivilege*</span><span class="sxs-lookup"><span data-stu-id="631e2-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="631e2-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="631e2-111">Required.</span></span> <span data-ttu-id="631e2-112">Uma das cadeias de caracteres de privilégio.</span><span class="sxs-lookup"><span data-stu-id="631e2-112">One of the privilege strings.</span></span> <span data-ttu-id="631e2-113">Para obter uma lista completa dessas cadeias de caracteres e as constantes do WMI associadas, consulte [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="631e2-114">Cada cadeia de caracteres de privilégio representa um privilégio específico.</span><span class="sxs-lookup"><span data-stu-id="631e2-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="631e2-115">Por exemplo, para adicionar o privilégio que usa para desligar um sistema de computador, use a cadeia de caracteres **SeShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="631e2-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="631e2-116">*bIsEnabled* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="631e2-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="631e2-117">Valor booliano que habilita ou desabilita esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="631e2-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="631e2-118">O valor padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="631e2-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="631e2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="631e2-119">Return value</span></span>

<span data-ttu-id="631e2-120">Se for bem-sucedido, esse método retornará um objeto [**SWbemPrivilege**](swbemprivilege.md) que representa o novo privilégio.</span><span class="sxs-lookup"><span data-stu-id="631e2-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="631e2-121">Caso contrário, um objeto nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="631e2-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="631e2-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="631e2-122">Error codes</span></span>

<span data-ttu-id="631e2-123">Após a conclusão do método **AddAsString** , o objeto **Err** pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="631e2-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="631e2-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="631e2-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="631e2-125">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="631e2-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="631e2-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="631e2-126">Examples</span></span>

<span data-ttu-id="631e2-127">O exemplo de código VBScript a seguir cria uma nova porta para um servidor de impressão usando o [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span><span class="sxs-lookup"><span data-stu-id="631e2-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="631e2-128">O **SeLoadDriverPrivilege** é necessário para esta operação.</span><span class="sxs-lookup"><span data-stu-id="631e2-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="631e2-129">Consulte [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="631e2-130">Um exemplo de código usando esse método também é descrito no tópico [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="631e2-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="631e2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="631e2-131">Requirements</span></span>



| <span data-ttu-id="631e2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="631e2-132">Requirement</span></span> | <span data-ttu-id="631e2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="631e2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="631e2-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="631e2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="631e2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="631e2-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="631e2-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="631e2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="631e2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="631e2-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="631e2-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="631e2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="631e2-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="631e2-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="631e2-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="631e2-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="631e2-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="631e2-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="631e2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="631e2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="631e2-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="631e2-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="631e2-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="631e2-144">CLSID</span></span><br/>                    | <span data-ttu-id="631e2-145">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="631e2-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="631e2-146">IID</span><span class="sxs-lookup"><span data-stu-id="631e2-146">IID</span></span><br/>                      | <span data-ttu-id="631e2-147">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="631e2-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="631e2-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="631e2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631e2-149">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="631e2-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="631e2-150">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="631e2-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="631e2-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="631e2-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="631e2-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="631e2-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="631e2-153">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="631e2-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="631e2-154">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="631e2-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="631e2-155">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="631e2-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

