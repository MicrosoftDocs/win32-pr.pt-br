---
title: ErrorItem.errorContext
description: A propriedade errorContext recupera um valor que indica o contexto do erro.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorContext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813163"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="450a6-104">ErrorItem.errorContext</span><span class="sxs-lookup"><span data-stu-id="450a6-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="450a6-105">A propriedade **errorContext** recupera um valor que indica o contexto do erro.</span><span class="sxs-lookup"><span data-stu-id="450a6-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="450a6-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="450a6-106">Possible Values</span></span>

<span data-ttu-id="450a6-107">Essa propriedade é uma **cadeia de caracteres** somente leitura que representa o código de contexto de erro.</span><span class="sxs-lookup"><span data-stu-id="450a6-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="450a6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="450a6-108">Remarks</span></span>

<span data-ttu-id="450a6-109">O contexto de erro é uma informação que é usada pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="450a6-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="450a6-110">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="450a6-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="450a6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="450a6-111">Requirements</span></span>



| <span data-ttu-id="450a6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="450a6-112">Requirement</span></span> | <span data-ttu-id="450a6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="450a6-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="450a6-114">Versão</span><span class="sxs-lookup"><span data-stu-id="450a6-114">Version</span></span><br/> | <span data-ttu-id="450a6-115">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="450a6-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="450a6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="450a6-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="450a6-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="450a6-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450a6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="450a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450a6-119">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="450a6-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





