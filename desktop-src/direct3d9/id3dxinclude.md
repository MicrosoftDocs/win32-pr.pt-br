---
description: ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para \# incluir diretivas durante a compilação do sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interface ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771475"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="43565-103">Interface ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="43565-103">ID3DXInclude interface</span></span>

<span data-ttu-id="43565-104">ID3DXInclude é uma interface implementada pelo usuário para fornecer retornos de chamada para \# incluir diretivas durante a compilação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="43565-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="43565-105">Cada um dos métodos nesta interface deve ser implementado pelo usuário que, em seguida, será usado como retornos de chamada para o aplicativo quando ocorrer uma das seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="43565-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="43565-106">Um sombreador HLSL que contém um \# include é compilado chamando uma das funções D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="43565-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="43565-107">Um sombreador de assembly \# incluído é montado chamando qualquer uma das \* \* \* funções D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="43565-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="43565-108">Um efeito que contém uma \# inclusão é compilado pelo chamando qualquer uma das funções D3DXCreateEffect \* \* \* ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="43565-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="43565-109">Membros</span><span class="sxs-lookup"><span data-stu-id="43565-109">Members</span></span>

<span data-ttu-id="43565-110">A interface **ID3DXInclude** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="43565-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="43565-111">**ID3DXInclude** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43565-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="43565-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="43565-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43565-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="43565-113">Methods</span></span>

<span data-ttu-id="43565-114">A interface **ID3DXInclude** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="43565-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="43565-115">Método</span><span class="sxs-lookup"><span data-stu-id="43565-115">Method</span></span>                               | <span data-ttu-id="43565-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="43565-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43565-117">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="43565-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="43565-118">Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="43565-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="43565-119">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="43565-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="43565-120">Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="43565-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43565-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="43565-121">Remarks</span></span>

<span data-ttu-id="43565-122">Um usuário cria uma interface ID3DXInclude implementando uma classe derivada dessa interface e implementando todos os métodos de interface.</span><span class="sxs-lookup"><span data-stu-id="43565-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="43565-123">O tipo LPD3DXINCLUDE é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="43565-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="43565-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43565-124">Requirements</span></span>



| <span data-ttu-id="43565-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="43565-125">Requirement</span></span> | <span data-ttu-id="43565-126">Valor</span><span class="sxs-lookup"><span data-stu-id="43565-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43565-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43565-127">Header</span></span><br/>  | <dl> <span data-ttu-id="43565-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="43565-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="43565-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43565-129">Library</span></span><br/> | <dl> <span data-ttu-id="43565-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43565-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="43565-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="43565-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43565-132">Interfaces de efeito</span><span class="sxs-lookup"><span data-stu-id="43565-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
