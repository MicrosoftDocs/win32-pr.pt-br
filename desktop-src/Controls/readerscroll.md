---
title: Função de retorno de chamada ReaderScroll
description: Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela do modo de leitor que foi declarada como a área de rolagem ativa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Controles do Windows da função de retorno de chamada ReaderScroll
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918386"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="7f319-104">Função de retorno de chamada ReaderScroll</span><span class="sxs-lookup"><span data-stu-id="7f319-104">ReaderScroll callback function</span></span>

<span data-ttu-id="7f319-105">\[O *ReaderScroll* está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="7f319-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7f319-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="7f319-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="7f319-107">Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela do modo de leitor que foi declarada como a área de rolagem ativa.</span><span class="sxs-lookup"><span data-stu-id="7f319-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f319-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f319-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="7f319-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f319-110">*prmi* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f319-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f319-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="7f319-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="7f319-112">Um ponteiro para a estrutura [**READERMODEINFO**](readermodeinfo.md) que foi passada para a função [**doreadermode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="7f319-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="7f319-113">Essa estrutura define a janela modo de leitura e a área de rolagem ativa.</span><span class="sxs-lookup"><span data-stu-id="7f319-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="7f319-114">*DX* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="7f319-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f319-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7f319-115">Type: **int**</span></span>

<span data-ttu-id="7f319-116">A distância para rolar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="7f319-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="7f319-117">Se o \_ sinalizador RMF VERTICALONLY for definido na estrutura [**READERMODEINFO**](readermodeinfo.md) , esse valor será sempre 0.</span><span class="sxs-lookup"><span data-stu-id="7f319-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="7f319-118">*DY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f319-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f319-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="7f319-119">Type: **int**</span></span>

<span data-ttu-id="7f319-120">A distância para rolar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="7f319-120">The distance to scroll vertically.</span></span> <span data-ttu-id="7f319-121">Se o \_ sinalizador RMF HORIZONTALONLY for definido na estrutura [**READERMODEINFO**](readermodeinfo.md) , esse valor será sempre 0.</span><span class="sxs-lookup"><span data-stu-id="7f319-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f319-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f319-122">Return value</span></span>

<span data-ttu-id="7f319-123">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7f319-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7f319-124">Essa função sempre deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="7f319-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f319-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f319-125">Remarks</span></span>

<span data-ttu-id="7f319-126">Quando o aplicativo recebe uma notificação dessa função, o aplicativo é responsável por rolar a janela do modo de leitura na direção especificada pelos parâmetros *DX* e *DY* .</span><span class="sxs-lookup"><span data-stu-id="7f319-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="7f319-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f319-127">Examples</span></span>

<span data-ttu-id="7f319-128">O exemplo a seguir descreve uma implementação dessa função usando uma função personalizada para realizar a rolagem.</span><span class="sxs-lookup"><span data-stu-id="7f319-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="7f319-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f319-129">Requirements</span></span>



| <span data-ttu-id="7f319-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f319-130">Requirement</span></span> | <span data-ttu-id="7f319-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7f319-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7f319-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f319-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7f319-133">Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f319-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7f319-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f319-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7f319-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f319-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

