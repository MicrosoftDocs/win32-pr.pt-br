---
title: Método RegisteredTask. GetSecurityDescriptor
description: Para scripts, obtém o descritor de segurança que é usado como credenciais para a tarefa registrada.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Agendador de Tarefas do método GetSecurityDescriptor
- Método GetSecurityDescriptor Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, Método GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918909"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="aa31c-106">Método RegisteredTask. GetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="aa31c-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="aa31c-107">Para scripts, obtém o descritor de segurança que é usado como credenciais para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="aa31c-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa31c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa31c-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="aa31c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa31c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa31c-110">*securityInformation*</span><span class="sxs-lookup"><span data-stu-id="aa31c-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="aa31c-111">As informações de segurança [**de \_ informações de segurança**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="aa31c-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa31c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa31c-112">Return value</span></span>

<span data-ttu-id="aa31c-113">O descritor de segurança para a tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="aa31c-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa31c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa31c-114">Requirements</span></span>



| <span data-ttu-id="aa31c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa31c-115">Requirement</span></span> | <span data-ttu-id="aa31c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="aa31c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa31c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa31c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa31c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa31c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa31c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa31c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa31c-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa31c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa31c-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa31c-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa31c-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa31c-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa31c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aa31c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa31c-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa31c-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa31c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa31c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa31c-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="aa31c-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="aa31c-127">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aa31c-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="aa31c-128">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="aa31c-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

