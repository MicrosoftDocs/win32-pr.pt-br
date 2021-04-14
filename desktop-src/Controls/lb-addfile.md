---
title: Mensagem de LB_ADDFILE (WinUser. h)
description: Adiciona o nome de arquivo especificado a uma caixa de listagem que contém uma listagem de diretório.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- Controles de LB_ADDFILE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455661"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="8fc4c-104">A \_ mensagem de ADDfile do lb</span><span class="sxs-lookup"><span data-stu-id="8fc4c-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="8fc4c-105">Adiciona o nome de arquivo especificado a uma caixa de listagem que contém uma listagem de diretório.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fc4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fc4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fc4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc4c-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8fc4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fc4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc4c-110">Um ponteiro para um buffer que especifica o nome do arquivo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc4c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fc4c-111">Return value</span></span>

<span data-ttu-id="8fc4c-112">O valor de retorno é o índice de base zero do arquivo que foi adicionado, ou erro de LB \_ se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc4c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fc4c-113">Remarks</span></span>

<span data-ttu-id="8fc4c-114">A caixa de listagem para a qual o *lParam* é adicionado deve ter sido preenchida pela função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .</span><span class="sxs-lookup"><span data-stu-id="8fc4c-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="8fc4c-115">A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="8fc4c-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="8fc4c-116">Ele reserva a quantidade especificada de memória para que as mensagens do **lb \_ AddFile** tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="8fc4c-117">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="8fc4c-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="8fc4c-118">Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="8fc4c-119">Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="8fc4c-120">Isso pode causar problemas.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-120">This can cause problems.</span></span> <span data-ttu-id="8fc4c-121">Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows em Japonês ficarão confusos.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="8fc4c-122">Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="8fc4c-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc4c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc4c-123">Requirements</span></span>



| <span data-ttu-id="8fc4c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc4c-124">Requirement</span></span> | <span data-ttu-id="8fc4c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc4c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc4c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc4c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc4c-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fc4c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fc4c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc4c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc4c-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fc4c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fc4c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc4c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc4c-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fc4c-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc4c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fc4c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="8fc4c-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8fc4c-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8fc4c-134">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="8fc4c-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="8fc4c-135">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="8fc4c-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





