---
title: Estrutura FONTGROUPHDR
description: Contém as informações necessárias para que um aplicativo acesse uma fonte específica. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menus de estrutura FONTGROUPHDR e outros recursos
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163611"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="b17d3-105">Estrutura FONTGROUPHDR</span><span class="sxs-lookup"><span data-stu-id="b17d3-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="b17d3-106">Contém as informações necessárias para que um aplicativo acesse uma fonte específica.</span><span class="sxs-lookup"><span data-stu-id="b17d3-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="b17d3-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="b17d3-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17d3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b17d3-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="b17d3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b17d3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b17d3-110">**NumberOfFonts**</span><span class="sxs-lookup"><span data-stu-id="b17d3-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="b17d3-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="b17d3-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b17d3-112">O número de fontes individuais associadas a este recurso.</span><span class="sxs-lookup"><span data-stu-id="b17d3-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="b17d3-113">**DEPRECIA**</span><span class="sxs-lookup"><span data-stu-id="b17d3-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="b17d3-114">Tipo: **[ **dialuguel**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="b17d3-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b17d3-115">Uma estrutura que contém um identificador ordinal exclusivo para cada fonte no recurso.</span><span class="sxs-lookup"><span data-stu-id="b17d3-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="b17d3-116">O membro **de** é um espaço reservado para a matriz de comprimento variável de estruturas de [**dialuguel**](direntry.md) .</span><span class="sxs-lookup"><span data-stu-id="b17d3-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b17d3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b17d3-117">Remarks</span></span>

<span data-ttu-id="b17d3-118">A estrutura **FONTGROUPHDR** segue os dados para as fontes individuais no. Arquivo Res.</span><span class="sxs-lookup"><span data-stu-id="b17d3-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="b17d3-119">O compilador de recurso adiciona automaticamente a estrutura **FONTGROUPHDR** , geralmente como a última entrada no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b17d3-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b17d3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17d3-120">Requirements</span></span>



| <span data-ttu-id="b17d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17d3-121">Requirement</span></span> | <span data-ttu-id="b17d3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b17d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b17d3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b17d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b17d3-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b17d3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b17d3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b17d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b17d3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b17d3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b17d3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b17d3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b17d3-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b17d3-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b17d3-129">**Dialugado**</span><span class="sxs-lookup"><span data-stu-id="b17d3-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="b17d3-130">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="b17d3-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="b17d3-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b17d3-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b17d3-132">Recursos</span><span class="sxs-lookup"><span data-stu-id="b17d3-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





