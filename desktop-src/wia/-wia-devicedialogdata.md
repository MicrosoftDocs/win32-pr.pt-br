---
description: Estrutura DEVICEDIALOGDATA – define os dados necessários para chamar uma caixa de diálogo de dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estrutura DEVICEDIALOGDATA (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104264"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="bd6d5-103">Estrutura DEVICEDIALOGDATA</span><span class="sxs-lookup"><span data-stu-id="bd6d5-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="bd6d5-104">Define os dados necessários para chamar uma caixa de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd6d5-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="bd6d5-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bd6d5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd6d5-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-109">Especifica o tamanho dessa estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="bd6d5-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-111">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-112">Especifica o identificador para a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="bd6d5-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-114">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span><span class="sxs-lookup"><span data-stu-id="bd6d5-114">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-115">Aponta para uma interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa o item raiz válido na árvore de itens de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-115">Points to an [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="bd6d5-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-118">Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="bd6d5-119">Pode ser definido como qualquer um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bd6d5-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="bd6d5-120">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="bd6d5-120">Flag</span></span>                                 | <span data-ttu-id="bd6d5-121">Significado</span><span class="sxs-lookup"><span data-stu-id="bd6d5-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6d5-122">0</span><span class="sxs-lookup"><span data-stu-id="bd6d5-122">0</span></span>                                    | <span data-ttu-id="bd6d5-123">Comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="bd6d5-124">\_ \_ imagem única da caixa de diálogo do dispositivo WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd6d5-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="bd6d5-125">Restringir a seleção de imagem a uma única imagem na caixa de diálogo aquisição de imagem de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="bd6d5-126">\_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum</span><span class="sxs-lookup"><span data-stu-id="bd6d5-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="bd6d5-127">Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="bd6d5-128">Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="bd6d5-129">Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="bd6d5-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-131">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-132">Especifica o tipo de dados que a imagem deve representar.</span><span class="sxs-lookup"><span data-stu-id="bd6d5-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="bd6d5-133">Para obter uma lista de valores de intenção de imagem, consulte [**constantes de objetivo de imagem**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="bd6d5-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd6d5-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-135">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-136">Recebe o número de itens na matriz indicado pelo parâmetro **ppWiaItem** .</span><span class="sxs-lookup"><span data-stu-id="bd6d5-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bd6d5-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="bd6d5-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="bd6d5-138">Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="bd6d5-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="bd6d5-139">Recebe o endereço de uma matriz de ponteiros para interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="bd6d5-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd6d5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd6d5-140">Requirements</span></span>



| <span data-ttu-id="bd6d5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6d5-141">Requirement</span></span> | <span data-ttu-id="bd6d5-142">Valor</span><span class="sxs-lookup"><span data-stu-id="bd6d5-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6d5-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd6d5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6d5-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd6d5-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bd6d5-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd6d5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6d5-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd6d5-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bd6d5-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd6d5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6d5-148"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6d5-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




