---
title: Método GetLastRestoreStatus da classe SystemRestore
description: Recupera o status da última restauração do sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Restauração do sistema do método GetLastRestoreStatus
- GetLastRestoreStatus método de restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763323"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="3e20c-106">Método GetLastRestoreStatus da classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="3e20c-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="3e20c-107">Recupera o status da última restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="3e20c-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e20c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e20c-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="3e20c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e20c-109">Parameters</span></span>

<span data-ttu-id="3e20c-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3e20c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e20c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e20c-111">Return value</span></span>

<span data-ttu-id="3e20c-112">O método retorna um dos valores de status a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e20c-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="3e20c-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3e20c-113">Return value</span></span>                                                                 | <span data-ttu-id="3e20c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e20c-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e20c-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e20c-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3e20c-116">A última restauração falhou.</span><span class="sxs-lookup"><span data-stu-id="3e20c-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="3e20c-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3e20c-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3e20c-118">A última restauração foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e20c-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="3e20c-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3e20c-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3e20c-120">A última restauração foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="3e20c-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="3e20c-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e20c-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="3e20c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e20c-122">Requirements</span></span>



| <span data-ttu-id="3e20c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e20c-123">Requirement</span></span> | <span data-ttu-id="3e20c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3e20c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3e20c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e20c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3e20c-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e20c-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e20c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e20c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3e20c-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e20c-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="3e20c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e20c-129">Namespace</span></span><br/>                | <span data-ttu-id="3e20c-130">\\Padrão raiz</span><span class="sxs-lookup"><span data-stu-id="3e20c-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="3e20c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3e20c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e20c-132"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e20c-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e20c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e20c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e20c-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="3e20c-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





