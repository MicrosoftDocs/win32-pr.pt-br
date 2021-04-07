---
description: O método remove do objeto SWbemPrivilegeSet exclui um privilégio da coleção.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828659"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="bcd46-103">Método SWbemPrivilegeSet. Remove</span><span class="sxs-lookup"><span data-stu-id="bcd46-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="bcd46-104">O método **Remove** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) exclui um privilégio da coleção.</span><span class="sxs-lookup"><span data-stu-id="bcd46-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="bcd46-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bcd46-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd46-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcd46-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="bcd46-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcd46-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd46-108">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="bcd46-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="bcd46-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="bcd46-109">Required.</span></span> <span data-ttu-id="bcd46-110">Essa é uma das constantes do WMI do grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="bcd46-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="bcd46-111">Essas constantes são essencialmente inteiros que representam privilégios específicos.</span><span class="sxs-lookup"><span data-stu-id="bcd46-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="bcd46-112">Por exemplo, para remover o privilégio que permite desligar um sistema Windows, use a constante **wbemPrivilegeShutdown** ou o equivalente numérico de 0x17.</span><span class="sxs-lookup"><span data-stu-id="bcd46-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd46-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcd46-113">Return value</span></span>

<span data-ttu-id="bcd46-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bcd46-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bcd46-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bcd46-115">Error codes</span></span>

<span data-ttu-id="bcd46-116">Após a conclusão do método **Remove** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcd46-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bcd46-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bcd46-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bcd46-118">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="bcd46-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bcd46-119">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="bcd46-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bcd46-120">O privilégio especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="bcd46-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcd46-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcd46-121">Requirements</span></span>



| <span data-ttu-id="bcd46-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd46-122">Requirement</span></span> | <span data-ttu-id="bcd46-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bcd46-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd46-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd46-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd46-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcd46-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcd46-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd46-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd46-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcd46-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcd46-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcd46-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcd46-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcd46-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bcd46-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bcd46-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcd46-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bcd46-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bcd46-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd46-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd46-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd46-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bcd46-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="bcd46-134">CLSID</span></span><br/>                    | <span data-ttu-id="bcd46-135">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="bcd46-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="bcd46-136">IID</span><span class="sxs-lookup"><span data-stu-id="bcd46-136">IID</span></span><br/>                      | <span data-ttu-id="bcd46-137">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="bcd46-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="bcd46-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcd46-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd46-139">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="bcd46-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="bcd46-140">**SWbemPrivilegeSet. Add**</span><span class="sxs-lookup"><span data-stu-id="bcd46-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




