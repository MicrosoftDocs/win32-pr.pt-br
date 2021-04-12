---
title: Propriedade de ícone IResultVerb (WdsSharedIDL. h)
description: Essa propriedade retorna um ponteiro para o identificador do ícone opcional associado ao verbo.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Propriedade Icon recursos de ambiente do Windows herdados
- Propriedade Icon recursos de ambiente do Windows herdados, interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, Propriedade Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455463"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="2afce-106">Propriedade IResultVerb:: icon</span><span class="sxs-lookup"><span data-stu-id="2afce-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="2afce-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2afce-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2afce-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2afce-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2afce-109">Essa propriedade retorna um ponteiro para o identificador do ícone opcional associado ao verbo.</span><span class="sxs-lookup"><span data-stu-id="2afce-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="2afce-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2afce-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afce-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2afce-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="2afce-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2afce-112">Property value</span></span>

<span data-ttu-id="2afce-113">HICON é um ponteiro para o identificador do ícone opcional assocuated com o verbo.</span><span class="sxs-lookup"><span data-stu-id="2afce-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2afce-114">Requirements</span></span>



| <span data-ttu-id="2afce-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2afce-115">Requirement</span></span> | <span data-ttu-id="2afce-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2afce-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2afce-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2afce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2afce-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="2afce-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2afce-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2afce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2afce-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="2afce-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2afce-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2afce-121">Redistributable</span></span><br/>          | <span data-ttu-id="2afce-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2afce-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2afce-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2afce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2afce-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2afce-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





