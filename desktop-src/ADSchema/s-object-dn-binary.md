---
title: Sintaxe de objeto (DN-binário)
description: Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome distinto).
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DN binário) do AD
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086563"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="ccf58-104">Sintaxe de objeto (DN-binário)</span><span class="sxs-lookup"><span data-stu-id="ccf58-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="ccf58-105">Uma cadeia de caracteres de octeto que contém um valor binário e um DN (nome distinto).</span><span class="sxs-lookup"><span data-stu-id="ccf58-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="ccf58-106">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccf58-106">Entry</span></span> | <span data-ttu-id="ccf58-107">Valor</span><span class="sxs-lookup"><span data-stu-id="ccf58-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf58-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ccf58-108">Name</span></span>         | <span data-ttu-id="ccf58-109">Objeto (DN-binário)</span><span class="sxs-lookup"><span data-stu-id="ccf58-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="ccf58-110">ID da sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccf58-110">Syntax ID</span></span>    | <span data-ttu-id="ccf58-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="ccf58-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="ccf58-112">ID DO OM</span><span class="sxs-lookup"><span data-stu-id="ccf58-112">OM ID</span></span>        | <span data-ttu-id="ccf58-113">127</span><span class="sxs-lookup"><span data-stu-id="ccf58-113">127</span></span>                                                                                |
| <span data-ttu-id="ccf58-114">Tipo de MAPI</span><span class="sxs-lookup"><span data-stu-id="ccf58-114">MAPI Type</span></span>    | <span data-ttu-id="ccf58-115">TSTRING</span><span class="sxs-lookup"><span data-stu-id="ccf58-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="ccf58-116">Tipo de ADS</span><span class="sxs-lookup"><span data-stu-id="ccf58-116">ADS Type</span></span>     | <span data-ttu-id="ccf58-117">\_DN ADSTYPE \_ com \_ binário</span><span class="sxs-lookup"><span data-stu-id="ccf58-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="ccf58-118">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="ccf58-118">Variant Type</span></span> | <span data-ttu-id="ccf58-119">expedição de VT \_</span><span class="sxs-lookup"><span data-stu-id="ccf58-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="ccf58-120">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="ccf58-120">SDS Type</span></span>     | <span data-ttu-id="ccf58-121">Um objeto COM que pode ser convertido em um [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span><span class="sxs-lookup"><span data-stu-id="ccf58-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="ccf58-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccf58-122">Remarks</span></span>

<span data-ttu-id="ccf58-123">Um valor com essa sintaxe tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="ccf58-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="ccf58-124">onde " &lt; contagem &gt; de caracteres" é o número de dígitos hexadecimais em " &lt; valor binário &gt; ", " &lt; valor binário &gt; " é a representação HEXADECIMAL do valor binário e "DN do &lt; objeto &gt; " é um nome diferenciado.</span><span class="sxs-lookup"><span data-stu-id="ccf58-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="ccf58-125">Active Directory atualizará automaticamente o DN se o objeto ao qual ele se refere for movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="ccf58-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="ccf58-126">Para obter mais informações e um exemplo de código que usa essa sintaxe, consulte [habilitando a associação de renomeação segura com a propriedade otherWellKnownObjects](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="ccf58-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="ccf58-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccf58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf58-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="ccf58-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
