---
description: Define a lista de IDs de grupo persistente para todos os perfis que são persistidos por seu aplicativo.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Função WFDDisplaySinkSetPersistedGroupIDList (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753138"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="885cb-103">Função WFDDisplaySinkSetPersistedGroupIDList</span><span class="sxs-lookup"><span data-stu-id="885cb-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="885cb-104">Define a lista de IDs de grupo persistente para todos os perfis que são persistidos por seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="885cb-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="885cb-105">Seu aplicativo deve chamar esse método toda vez que adicionar ou excluir um perfil de seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="885cb-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="885cb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="885cb-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="885cb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="885cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885cb-108">*cGroupIDList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="885cb-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885cb-109">A contagem de IDs de grupo que está sendo apontada por *pGroupIDList*.</span><span class="sxs-lookup"><span data-stu-id="885cb-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="885cb-110">*pGroupIDList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="885cb-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885cb-111">Ponteiro para uma matriz de IDs de grupo *cGroupIDList* .</span><span class="sxs-lookup"><span data-stu-id="885cb-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885cb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="885cb-112">Return value</span></span>

<span data-ttu-id="885cb-113">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="885cb-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="885cb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="885cb-114">Remarks</span></span>

<span data-ttu-id="885cb-115">Esse método sempre deve ser chamado com a lista inteira e não um subconjunto.</span><span class="sxs-lookup"><span data-stu-id="885cb-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="885cb-116">OK para chamar esse método com 0 perfis quando o repositório de perfis estiver vazio.</span><span class="sxs-lookup"><span data-stu-id="885cb-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="885cb-117">Uma reinvocação para uma ID de grupo que não faz parte da lista fornecida falhará com "falha; Grupo P2P desconhecido "(status 8).</span><span class="sxs-lookup"><span data-stu-id="885cb-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="885cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="885cb-118">Requirements</span></span>



| <span data-ttu-id="885cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="885cb-119">Requirement</span></span> | <span data-ttu-id="885cb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="885cb-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="885cb-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="885cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="885cb-122">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="885cb-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="885cb-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="885cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="885cb-124">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="885cb-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="885cb-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="885cb-125">End of client support</span></span><br/>    | <span data-ttu-id="885cb-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="885cb-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="885cb-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="885cb-127">End of server support</span></span><br/>    | <span data-ttu-id="885cb-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="885cb-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="885cb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="885cb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="885cb-130"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="885cb-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="885cb-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="885cb-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="885cb-132"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="885cb-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="885cb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="885cb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="885cb-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="885cb-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




