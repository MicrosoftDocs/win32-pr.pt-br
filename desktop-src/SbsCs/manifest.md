---
description: A propriedade de manifesto é usada para definir ou obter o contexto de ativação ativa.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propriedade ActCtx. manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920830"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="37d30-103">Propriedade ActCtx. manifest</span><span class="sxs-lookup"><span data-stu-id="37d30-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="37d30-104">A propriedade de **manifesto** é usada para definir ou obter o contexto de ativação ativa.</span><span class="sxs-lookup"><span data-stu-id="37d30-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="37d30-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="37d30-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d30-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37d30-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="37d30-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="37d30-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="37d30-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="37d30-108">Remarks</span></span>

<span data-ttu-id="37d30-109">Se um contexto de ativação puder ser criado com o arquivo de manifesto fornecido, o script a seguir definirá a propriedade de manifesto e ativará a constante de ativação especificada pelo manifesto.</span><span class="sxs-lookup"><span data-stu-id="37d30-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="37d30-110">Se um contexto de ativação não puder ser criado a partir do manifesto, o contexto de ativação permanecerá definido como o contexto de ativação ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="37d30-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="37d30-111">ActCtxObj. manifest = "<*nome do arquivo de manifesto*>";</span><span class="sxs-lookup"><span data-stu-id="37d30-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="37d30-112">Se um contexto de ativação tiver sido criado ou ativado anteriormente, o script a seguir definirá a propriedade de **manifesto** como o contexto de ativação atual.</span><span class="sxs-lookup"><span data-stu-id="37d30-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="37d30-113">Se um contexto de ativação não tiver sido criado ou ativado anteriormente, isso definirá a propriedade de **manifesto** como uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="37d30-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="37d30-114">"BSTR bstrManifest = ActCtxObj. manifest"</span><span class="sxs-lookup"><span data-stu-id="37d30-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="37d30-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37d30-115">Requirements</span></span>



| <span data-ttu-id="37d30-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d30-116">Requirement</span></span> | <span data-ttu-id="37d30-117">Valor</span><span class="sxs-lookup"><span data-stu-id="37d30-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="37d30-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37d30-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37d30-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37d30-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="37d30-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37d30-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37d30-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37d30-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="37d30-122">DLL</span><span class="sxs-lookup"><span data-stu-id="37d30-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d30-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d30-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="37d30-124">IID</span><span class="sxs-lookup"><span data-stu-id="37d30-124">IID</span></span><br/>                      | <span data-ttu-id="37d30-125">IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="37d30-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




