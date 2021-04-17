---
description: O método DeleteAll do objeto SWbemPrivilegeSet remove todos os privilégios da coleção, esvaziando-os.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783791"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="b8414-103">Método SWbemPrivilegeSet. DeleteAll</span><span class="sxs-lookup"><span data-stu-id="b8414-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="b8414-104">O método **DeleteAll** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) remove todos os privilégios da coleção, esvaziando-os.</span><span class="sxs-lookup"><span data-stu-id="b8414-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8414-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8414-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="b8414-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8414-106">Parameters</span></span>

<span data-ttu-id="b8414-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b8414-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8414-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8414-108">Return value</span></span>

<span data-ttu-id="b8414-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b8414-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8414-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b8414-110">Error codes</span></span>

<span data-ttu-id="b8414-111">Após a conclusão do método **DeleteAll** , o objeto **Err** pode conter o código de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="b8414-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b8414-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b8414-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b8414-113">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b8414-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8414-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8414-114">Requirements</span></span>



| <span data-ttu-id="b8414-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8414-115">Requirement</span></span> | <span data-ttu-id="b8414-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b8414-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8414-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8414-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8414-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8414-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8414-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8414-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8414-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8414-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8414-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8414-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8414-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8414-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8414-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b8414-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b8414-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b8414-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b8414-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8414-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8414-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8414-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8414-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="b8414-127">CLSID</span></span><br/>                    | <span data-ttu-id="b8414-128">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="b8414-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="b8414-129">IID</span><span class="sxs-lookup"><span data-stu-id="b8414-129">IID</span></span><br/>                      | <span data-ttu-id="b8414-130">ISWbemPrivilegeSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="b8414-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="b8414-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8414-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8414-132">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="b8414-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="b8414-133">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="b8414-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="b8414-134">**SWbemPrivilegeSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="b8414-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




