---
title: Método Session. Delete (WSManDisp. h)
description: Exclui o recurso especificado no URI de recurso.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Delete
- Gerenciamento Remoto do Windows do método Delete, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, método Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918180"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="7190d-106">Método Session. Delete</span><span class="sxs-lookup"><span data-stu-id="7190d-106">Session.Delete method</span></span>

<span data-ttu-id="7190d-107">Exclui o recurso especificado no URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="7190d-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="7190d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7190d-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7190d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7190d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7190d-110">*ResourceURI* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7190d-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7190d-111">O URI do recurso a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7190d-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="7190d-112">Você também pode usar um objeto [**ResourceLocator**](resourcelocator.md) para especificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7190d-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7190d-113">*sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7190d-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7190d-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7190d-114">Reserved for future use.</span></span> <span data-ttu-id="7190d-115">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="7190d-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7190d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7190d-116">Return value</span></span>

<span data-ttu-id="7190d-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7190d-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7190d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7190d-118">Remarks</span></span>

<span data-ttu-id="7190d-119">A sintaxe a seguir é usada para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7190d-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="7190d-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7190d-120">Examples</span></span>

<span data-ttu-id="7190d-121">O exemplo de código VBScript a seguir exclui os ouvintes configurados para transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="7190d-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="7190d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7190d-122">Requirements</span></span>



| <span data-ttu-id="7190d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7190d-123">Requirement</span></span> | <span data-ttu-id="7190d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7190d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7190d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7190d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7190d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7190d-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7190d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7190d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7190d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7190d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7190d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7190d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7190d-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7190d-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7190d-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="7190d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7190d-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7190d-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7190d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7190d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7190d-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7190d-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7190d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7190d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7190d-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7190d-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7190d-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7190d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7190d-138">**Session**</span><span class="sxs-lookup"><span data-stu-id="7190d-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





