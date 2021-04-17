---
title: Enumeração COLORtype (Softkbdc. h)
description: Os elementos da enumeração COLORtype são usados para especificar tipos de cores que estão disponíveis para um teclado virtual.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Estrutura de serviços de texto de enumeração COLORtype
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755527"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="1b241-104">Enumeração COLORtype</span><span class="sxs-lookup"><span data-stu-id="1b241-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="1b241-105">Os elementos da enumeração **ColorType** são usados para especificar tipos de cores que estão disponíveis para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="1b241-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b241-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b241-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="1b241-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1b241-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1b241-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="1b241-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-109">Cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1b241-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="1b241-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span><span class="sxs-lookup"><span data-stu-id="1b241-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-111">Cor de primeiro plano não selecionada.</span><span class="sxs-lookup"><span data-stu-id="1b241-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="1b241-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span><span class="sxs-lookup"><span data-stu-id="1b241-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-113">Cor do texto não selecionada.</span><span class="sxs-lookup"><span data-stu-id="1b241-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="1b241-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span><span class="sxs-lookup"><span data-stu-id="1b241-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-115">Cor de primeiro plano selecionada.</span><span class="sxs-lookup"><span data-stu-id="1b241-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="1b241-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span><span class="sxs-lookup"><span data-stu-id="1b241-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-117">Cor do texto selecionada.</span><span class="sxs-lookup"><span data-stu-id="1b241-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="1b241-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo de cor máximo \_**</span><span class="sxs-lookup"><span data-stu-id="1b241-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="1b241-119">Tipo de cor máximo.</span><span class="sxs-lookup"><span data-stu-id="1b241-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b241-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b241-120">Requirements</span></span>



| <span data-ttu-id="1b241-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b241-121">Requirement</span></span> | <span data-ttu-id="1b241-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1b241-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b241-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b241-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1b241-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b241-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1b241-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b241-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1b241-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b241-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b241-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1b241-127">Redistributable</span></span><br/>          | <span data-ttu-id="1b241-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1b241-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1b241-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b241-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b241-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b241-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1b241-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="1b241-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b241-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b241-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





