---
description: Estende o objeto IShellDispatch com uma variedade de novas funcionalidades.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objeto IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967520"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="5da2b-103">Objeto IShellDispatch2</span><span class="sxs-lookup"><span data-stu-id="5da2b-103">IShellDispatch2 object</span></span>

<span data-ttu-id="5da2b-104">Estende o objeto [**IShellDispatch**](ishelldispatch.md) com uma variedade de novas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="5da2b-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="5da2b-105">**IShellDispatch2** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="5da2b-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="5da2b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5da2b-106">Members</span></span>

<span data-ttu-id="5da2b-107">O objeto **IShellDispatch2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5da2b-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="5da2b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5da2b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5da2b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5da2b-109">Methods</span></span>

<span data-ttu-id="5da2b-110">O objeto **IShellDispatch2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5da2b-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="5da2b-111">Método</span><span class="sxs-lookup"><span data-stu-id="5da2b-111">Method</span></span>                                                               | <span data-ttu-id="5da2b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5da2b-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5da2b-113">**CanStartStopService**</span><span class="sxs-lookup"><span data-stu-id="5da2b-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="5da2b-114">Determina se o usuário atual pode iniciar e parar o serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="5da2b-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="5da2b-115">**FindPrinter**</span><span class="sxs-lookup"><span data-stu-id="5da2b-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="5da2b-116">Exibe a caixa de diálogo **Localizar impressora** .</span><span class="sxs-lookup"><span data-stu-id="5da2b-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="5da2b-117">**GetSystemInformation**</span><span class="sxs-lookup"><span data-stu-id="5da2b-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="5da2b-118">Recupera informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="5da2b-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="5da2b-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="5da2b-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="5da2b-120">Recupera a configuração de restrição de um grupo do registro.</span><span class="sxs-lookup"><span data-stu-id="5da2b-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="5da2b-121">**IsServiceRunning**</span><span class="sxs-lookup"><span data-stu-id="5da2b-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="5da2b-122">Retorna um valor que indica se um serviço específico está em execução.</span><span class="sxs-lookup"><span data-stu-id="5da2b-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="5da2b-123">**Iniciar**</span><span class="sxs-lookup"><span data-stu-id="5da2b-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="5da2b-124">Inicia um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="5da2b-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="5da2b-125">**Parar**</span><span class="sxs-lookup"><span data-stu-id="5da2b-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="5da2b-126">Interrompe um serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="5da2b-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="5da2b-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="5da2b-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="5da2b-128">Executa uma operação especificada em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5da2b-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="5da2b-129">**ShowBrowserBar**</span><span class="sxs-lookup"><span data-stu-id="5da2b-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="5da2b-130">Exibe uma barra de navegador.</span><span class="sxs-lookup"><span data-stu-id="5da2b-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5da2b-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5da2b-131">Remarks</span></span>

<span data-ttu-id="5da2b-132">Para obter uma discussão sobre os serviços do Windows, consulte a documentação de [Serviços](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="5da2b-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da2b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da2b-133">Requirements</span></span>



| <span data-ttu-id="5da2b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da2b-134">Requirement</span></span> | <span data-ttu-id="5da2b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5da2b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da2b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da2b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5da2b-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5da2b-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5da2b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5da2b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5da2b-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5da2b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5da2b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5da2b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5da2b-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5da2b-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5da2b-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="5da2b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5da2b-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5da2b-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5da2b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5da2b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da2b-145"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5da2b-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da2b-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="5da2b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da2b-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5da2b-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="5da2b-148">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="5da2b-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="5da2b-149">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="5da2b-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
