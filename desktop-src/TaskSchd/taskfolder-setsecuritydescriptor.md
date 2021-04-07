---
title: Propriedade TaskFolder. SetSecurityDescriptor
description: Para scripts, define o descritor de segurança para a pasta.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Agendador de Tarefas da propriedade SetSecurityDescriptor
- Propriedade SetSecurityDescriptor Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918216"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="ee479-106">Propriedade TaskFolder. SetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="ee479-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="ee479-107">Para scripts, define o descritor de segurança para a pasta.</span><span class="sxs-lookup"><span data-stu-id="ee479-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee479-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee479-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="ee479-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee479-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ee479-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee479-110">Remarks</span></span>

<span data-ttu-id="ee479-111">Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma pasta de tarefas a fim de permitir ou negar o acesso de determinados usuários e grupos a uma pasta de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ee479-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee479-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee479-112">Requirements</span></span>



| <span data-ttu-id="ee479-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee479-113">Requirement</span></span> | <span data-ttu-id="ee479-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ee479-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee479-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee479-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ee479-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee479-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ee479-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee479-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ee479-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee479-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee479-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ee479-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee479-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee479-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee479-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ee479-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee479-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee479-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee479-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee479-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee479-124">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ee479-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="ee479-125">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ee479-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





