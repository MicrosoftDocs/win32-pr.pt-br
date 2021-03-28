---
description: Atualiza um objeto passando um ponteiro para uma matriz de dois ponteiros para listas de identificadores de item (PIDLs). Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_UPDATEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172069"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="285ab-104">\_Mensagem SFVM UpdateObject</span><span class="sxs-lookup"><span data-stu-id="285ab-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="285ab-105">Atualiza um objeto passando um ponteiro para uma matriz de dois ponteiros para listas de identificadores de item (PIDLs).</span><span class="sxs-lookup"><span data-stu-id="285ab-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="285ab-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="285ab-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="285ab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="285ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285ab-108">*ppidl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="285ab-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285ab-109">O endereço de uma matriz de dois PIDLs.</span><span class="sxs-lookup"><span data-stu-id="285ab-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="285ab-110">O primeiro PIDL é o antigo PIDL.</span><span class="sxs-lookup"><span data-stu-id="285ab-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="285ab-111">A segunda é uma cópia do antigo PIDL com informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="285ab-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="285ab-112">O controle sobre o tempo de vida da cópia pertence ao modo de exibição após a conclusão bem-sucedida desta chamada.</span><span class="sxs-lookup"><span data-stu-id="285ab-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285ab-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="285ab-113">Return value</span></span>

<span data-ttu-id="285ab-114">Retorna a ID de ListView do objeto atualizado se a atualização foi bem-sucedida; caso contrário, retornará-1.</span><span class="sxs-lookup"><span data-stu-id="285ab-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="285ab-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="285ab-115">Remarks</span></span>

<span data-ttu-id="285ab-116">Se a atualização não tiver sido bem-sucedida, o chamador deverá liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="285ab-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="285ab-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="285ab-117">Requirements</span></span>



| <span data-ttu-id="285ab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="285ab-118">Requirement</span></span> | <span data-ttu-id="285ab-119">Valor</span><span class="sxs-lookup"><span data-stu-id="285ab-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="285ab-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="285ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="285ab-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="285ab-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="285ab-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="285ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="285ab-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="285ab-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="285ab-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="285ab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="285ab-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="285ab-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




