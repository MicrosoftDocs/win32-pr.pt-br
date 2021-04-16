---
title: Propriedade TaskFolder. GetSecurityDescriptor
description: Para scripts, obtém o descritor de segurança para a pasta.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Agendador de Tarefas da propriedade GetSecurityDescriptor
- Propriedade GetSecurityDescriptor Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758106"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="13e1d-106">Propriedade TaskFolder. GetSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="13e1d-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="13e1d-107">Para scripts, obtém o descritor de segurança para a pasta.</span><span class="sxs-lookup"><span data-stu-id="13e1d-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e1d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e1d-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="13e1d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="13e1d-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="13e1d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13e1d-110">Requirements</span></span>



| <span data-ttu-id="13e1d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e1d-111">Requirement</span></span> | <span data-ttu-id="13e1d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="13e1d-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e1d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13e1d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="13e1d-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13e1d-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13e1d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13e1d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="13e1d-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13e1d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13e1d-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="13e1d-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="13e1d-118"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="13e1d-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="13e1d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="13e1d-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e1d-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e1d-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e1d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="13e1d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e1d-122">**TaskFolder.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="13e1d-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="13e1d-123">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="13e1d-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





