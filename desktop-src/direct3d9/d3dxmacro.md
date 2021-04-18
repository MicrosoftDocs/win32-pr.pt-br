---
description: Descreve as definições de pré-processador usadas por um objeto de efeito.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Estrutura D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784625"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="b2152-103">Estrutura D3DXMACRO</span><span class="sxs-lookup"><span data-stu-id="b2152-103">D3DXMACRO structure</span></span>

<span data-ttu-id="b2152-104">Descreve as definições de pré-processador usadas por um objeto de efeito.</span><span class="sxs-lookup"><span data-stu-id="b2152-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2152-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2152-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="b2152-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b2152-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2152-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b2152-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="b2152-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2152-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2152-109">Nome do pré-processador.</span><span class="sxs-lookup"><span data-stu-id="b2152-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="b2152-110">**Definição**</span><span class="sxs-lookup"><span data-stu-id="b2152-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="b2152-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2152-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b2152-112">Nome da definição.</span><span class="sxs-lookup"><span data-stu-id="b2152-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2152-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2152-113">Remarks</span></span>

<span data-ttu-id="b2152-114">Para usar **D3DXMACRO** s em mais de uma linha, Prefixe cada caractere de nova linha com uma barra invertida (como uma \# definição na linguagem C).</span><span class="sxs-lookup"><span data-stu-id="b2152-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="b2152-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b2152-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="b2152-116">Observe os 3 caracteres de barra invertida no final da linha.</span><span class="sxs-lookup"><span data-stu-id="b2152-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="b2152-117">Os dois primeiros são necessários para gerar um único ' \\ ', seguido pelo caractere de nova linha " \\ n".</span><span class="sxs-lookup"><span data-stu-id="b2152-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="b2152-118">Opcionalmente, você também pode querer encerrar suas linhas usando " \\ \\ \\ r \\ n".</span><span class="sxs-lookup"><span data-stu-id="b2152-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="b2152-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2152-119">Requirements</span></span>



| <span data-ttu-id="b2152-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2152-120">Requirement</span></span> | <span data-ttu-id="b2152-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b2152-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2152-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2152-122">Header</span></span><br/> | <dl> <span data-ttu-id="b2152-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2152-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2152-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2152-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2152-125">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="b2152-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="b2152-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="b2152-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
