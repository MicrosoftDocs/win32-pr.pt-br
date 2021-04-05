---
title: Função ImageList_SetColorTable
description: Define a tabela de cores para uma lista de imagens.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Controles do Windows da função ImageList_SetColorTable
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919249"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="5fa71-104">\_Função ImageList Setcolortable</span><span class="sxs-lookup"><span data-stu-id="5fa71-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="5fa71-105">Define a tabela de cores para uma lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="5fa71-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa71-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fa71-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="5fa71-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fa71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa71-108">*himl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa71-109">Tipo: **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="5fa71-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="5fa71-110">Um identificador para a lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="5fa71-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="5fa71-111">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa71-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5fa71-112">Type: **int**</span></span>

<span data-ttu-id="5fa71-113">Um índice de tabela de cores com base em zero que especifica a primeira entrada da tabela de cores a ser definida.</span><span class="sxs-lookup"><span data-stu-id="5fa71-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="5fa71-114">*Len* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa71-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5fa71-115">Type: **int**</span></span>

<span data-ttu-id="5fa71-116">O número de entradas da tabela de cores a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="5fa71-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="5fa71-117">*prgb* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fa71-118">Tipo: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="5fa71-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="5fa71-119">Um ponteiro para uma matriz de _len \* estruturas [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) que contêm novas informações de cor para a tabela de cores do DIB.</span><span class="sxs-lookup"><span data-stu-id="5fa71-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa71-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fa71-120">Return value</span></span>

<span data-ttu-id="5fa71-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5fa71-121">Type: **int**</span></span>

<span data-ttu-id="5fa71-122">Se a função for realizada com sucesso, ela retornará o número de entradas da tabela de cores definidas pela função.</span><span class="sxs-lookup"><span data-stu-id="5fa71-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="5fa71-123">Se a função falhar, o valor de retorno será menor ou igual a zero.</span><span class="sxs-lookup"><span data-stu-id="5fa71-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fa71-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fa71-124">Remarks</span></span>

<span data-ttu-id="5fa71-125">Somente as listas de imagens criadas com o sinalizador [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ou [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) têm tabelas de cores.</span><span class="sxs-lookup"><span data-stu-id="5fa71-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="5fa71-126">A tabela de cores dessa lista de imagens normalmente é definida automaticamente copiando a tabela de cores da primeira imagem adicionada à lista (por exemplo, por meio da função [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) se essa imagem for uma DIB.</span><span class="sxs-lookup"><span data-stu-id="5fa71-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="5fa71-127">Se a primeira imagem adicionada à lista de imagens não for uma DIB, a tabela de cores da paleta de retícula será usada para listas de imagens **ILC \_ COLOR8** e a tabela de cores VGA será usada para **ILC \_ COLOR4**.</span><span class="sxs-lookup"><span data-stu-id="5fa71-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa71-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fa71-128">Requirements</span></span>



| <span data-ttu-id="5fa71-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa71-129">Requirement</span></span> | <span data-ttu-id="5fa71-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5fa71-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa71-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fa71-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa71-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="5fa71-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fa71-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa71-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fa71-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5fa71-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa71-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fa71-136"><dt>Comctl32.dll (versão 3,51 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa71-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa71-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fa71-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fa71-138">[Tabela de cores](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5fa71-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 

