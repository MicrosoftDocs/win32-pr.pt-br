---
description: A função GetDialogSize recupera o tamanho de uma caixa de diálogo de recurso.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Função GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752677"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="ce4e4-103">Função GetDialogSize</span><span class="sxs-lookup"><span data-stu-id="ce4e4-103">GetDialogSize function</span></span>

<span data-ttu-id="ce4e4-104">A função **GetDialogSize** recupera o tamanho de uma caixa de diálogo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce4e4-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="ce4e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce4e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce4e4-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="ce4e4-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4e4-108">Identificador de recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e4-109">*pDlgProc*</span><span class="sxs-lookup"><span data-stu-id="ce4e4-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4e4-110">Ponteiro para o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce4e4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4e4-112">Valor passado na mensagem do WM \_ INITDIALOG enviada para a caixa de diálogo temporária logo após sua criação.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e4-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="ce4e4-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="ce4e4-114">Ponteiro para uma estrutura de **tamanho** que recebe as dimensões da caixa de diálogo, na tela pixels.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce4e4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce4e4-115">Return value</span></span>

<span data-ttu-id="ce4e4-116">Retorna **true** se o recurso da caixa de diálogo foi encontrado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4e4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce4e4-117">Remarks</span></span>

<span data-ttu-id="ce4e4-118">As páginas de propriedades podem usar essa função para retornar o tamanho de exibição real necessário.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="ce4e4-119">A maioria das páginas de propriedades são caixas de diálogo e, como tal, têm modelos de caixa de diálogo armazenados em arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="ce4e4-120">Os modelos usam unidades de caixa de diálogo que não são mapeadas diretamente na tela pixels.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="ce4e4-121">No entanto, a função [**GetPageInfo**](cbasepropertypage-getpageinfo.md) de uma página de propriedades deve retornar o tamanho de exibição real em pixels.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="ce4e4-122">A página de propriedades pode chamar `GetDialogSize` para calcular o tamanho de exibição.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="ce4e4-123">Essa função cria uma instância temporária da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="ce4e4-124">Para evitar que a caixa de diálogo apareça na tela, o modelo de caixa de diálogo no arquivo de recurso não deve ter uma \_ Propriedade WS visível.</span><span class="sxs-lookup"><span data-stu-id="ce4e4-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4e4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4e4-125">Requirements</span></span>



| <span data-ttu-id="ce4e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4e4-126">Requirement</span></span> | <span data-ttu-id="ce4e4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ce4e4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4e4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce4e4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ce4e4-129"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e4-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce4e4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce4e4-130">Library</span></span><br/> | <dl> <span data-ttu-id="ce4e4-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4e4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce4e4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4e4-133">Funções auxiliares de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="ce4e4-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




