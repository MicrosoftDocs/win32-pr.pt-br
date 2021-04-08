---
description: O método Add do objeto SWbemPrivilegeSet adiciona um objeto SWbemPrivilege à coleção SWbemPrivilegeSet. Se já existir um privilégio com o mesmo nome na coleção, ele será substituído.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010759"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="8b650-104">Método SWbemPrivilegeSet. Add</span><span class="sxs-lookup"><span data-stu-id="8b650-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="8b650-105">O método **Add** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="8b650-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="8b650-106">Se já existir um privilégio com o mesmo nome na coleção, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="8b650-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="8b650-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8b650-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b650-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b650-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8b650-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b650-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b650-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="8b650-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="8b650-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8b650-111">Required.</span></span> <span data-ttu-id="8b650-112">Uma das constantes do WMI do grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="8b650-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="8b650-113">Essas constantes são essencialmente inteiros que representam privilégios específicos.</span><span class="sxs-lookup"><span data-stu-id="8b650-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="8b650-114">Por exemplo, para adicionar o privilégio que permite desligar um sistema de computador, use a constante **wbemPrivilegeShutdown** .</span><span class="sxs-lookup"><span data-stu-id="8b650-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="8b650-115">Em um script, você deve usar o equivalente numérico de 23 (0x17).</span><span class="sxs-lookup"><span data-stu-id="8b650-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="8b650-116">Para obter uma lista completa dessas constantes e as cadeias de caracteres de privilégio associadas, consulte [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8b650-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b650-117">*bIsEnabled* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="8b650-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b650-118">Valor booliano que habilita ou desabilita esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="8b650-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="8b650-119">O valor padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="8b650-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b650-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b650-120">Return value</span></span>

<span data-ttu-id="8b650-121">Se for bem-sucedido, o método retornará um objeto [**SWbemPrivilege**](swbemprivilege.md) que representa o novo privilégio.</span><span class="sxs-lookup"><span data-stu-id="8b650-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="8b650-122">Caso contrário, um objeto nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="8b650-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b650-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8b650-123">Error codes</span></span>

<span data-ttu-id="8b650-124">Após a conclusão do método **Add** , o objeto **Err** pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b650-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8b650-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8b650-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8b650-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8b650-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8b650-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b650-127">Examples</span></span>

<span data-ttu-id="8b650-128">Um exemplo de código usando esse método é descrito no tópico [**SWbemPrivilegeSet**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="8b650-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b650-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b650-129">Requirements</span></span>



| <span data-ttu-id="8b650-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b650-130">Requirement</span></span> | <span data-ttu-id="8b650-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8b650-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b650-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b650-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8b650-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b650-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b650-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b650-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8b650-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b650-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b650-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b650-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b650-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b650-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b650-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8b650-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b650-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b650-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b650-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8b650-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b650-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b650-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b650-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="8b650-142">CLSID</span></span><br/>                    | <span data-ttu-id="8b650-143">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="8b650-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="8b650-144">IID</span><span class="sxs-lookup"><span data-stu-id="8b650-144">IID</span></span><br/>                      | <span data-ttu-id="8b650-145">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="8b650-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="8b650-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b650-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b650-147">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="8b650-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="8b650-148">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="8b650-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="8b650-149">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="8b650-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="8b650-150">**SWbemPrivilegeSet.AddAsString**</span><span class="sxs-lookup"><span data-stu-id="8b650-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="8b650-151">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="8b650-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="8b650-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="8b650-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="8b650-153">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="8b650-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




