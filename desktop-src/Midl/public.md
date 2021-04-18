---
title: atributo público
description: O atributo \ Public \ inclui um alias declarado com a palavra-chave typedef na biblioteca de tipos.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- atributo público MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752058"
---
# <a name="public-attribute"></a><span data-ttu-id="0fc15-104">atributo público</span><span class="sxs-lookup"><span data-stu-id="0fc15-104">public attribute</span></span>

<span data-ttu-id="0fc15-105">O atributo **\[ \] Public** inclui um alias declarado com a palavra-chave [**typedef**](typedef.md) na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0fc15-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="0fc15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fc15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc15-107">*tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="0fc15-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc15-108">O tipo de dados para o qual o identificador será um alias.</span><span class="sxs-lookup"><span data-stu-id="0fc15-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="0fc15-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="0fc15-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0fc15-110">Outro nome pelo qual o *tipo de dados* será conhecido no software.</span><span class="sxs-lookup"><span data-stu-id="0fc15-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fc15-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fc15-111">Remarks</span></span>

<span data-ttu-id="0fc15-112">Por padrão, um alias declarado com [**typedef**](typedef.md) e nenhum outro atributo é tratado como uma **\# definição** e não é incluído na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0fc15-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="0fc15-113">O uso do atributo **\[ Public \]** garante que o alias se torne parte da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="0fc15-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="0fc15-114">O compilador MIDL requer que você aplique explicitamente o atributo **\[ Public \]** a cada TypeDef que você deseja público.</span><span class="sxs-lookup"><span data-stu-id="0fc15-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0fc15-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0fc15-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="0fc15-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fc15-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc15-117">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="0fc15-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="0fc15-118">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="0fc15-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="0fc15-119">**interface**</span><span class="sxs-lookup"><span data-stu-id="0fc15-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="0fc15-120">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="0fc15-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="0fc15-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0fc15-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 