---
title: Mensagem de WM_COPYDATA (WinUser. h)
description: Um aplicativo envia a mensagem do WM \_ CopyData para passar dados para outro aplicativo.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Troca de dados de mensagem WM_COPYDATA
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455300"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="4d349-104">Mensagem do WM \_ CopyData</span><span class="sxs-lookup"><span data-stu-id="4d349-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="4d349-105">Um aplicativo envia a mensagem do **WM \_ CopyData** para passar dados para outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d349-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="4d349-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d349-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d349-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d349-108">Um identificador para a janela que passa os dados.</span><span class="sxs-lookup"><span data-stu-id="4d349-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="4d349-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d349-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d349-110">Um ponteiro para uma estrutura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) que contém os dados a serem passados.</span><span class="sxs-lookup"><span data-stu-id="4d349-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d349-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d349-111">Return value</span></span>

<span data-ttu-id="4d349-112">Se o aplicativo de recebimento processar essa mensagem, ele deverá retornar **true**; caso contrário, ele deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="4d349-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d349-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d349-113">Remarks</span></span>

<span data-ttu-id="4d349-114">Os dados que estão sendo passados não devem conter ponteiros ou outras referências a objetos não acessíveis para o aplicativo que está recebendo os dados.</span><span class="sxs-lookup"><span data-stu-id="4d349-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="4d349-115">Enquanto essa mensagem está sendo enviada, os dados referenciados não devem ser alterados por outro thread do processo de envio.</span><span class="sxs-lookup"><span data-stu-id="4d349-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="4d349-116">O aplicativo de recebimento deve considerar os dados como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4d349-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="4d349-117">O parâmetro *lParam* é válido somente durante o processamento da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d349-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="4d349-118">O aplicativo de recebimento não deve liberar a memória referenciada pelo *lParam*.</span><span class="sxs-lookup"><span data-stu-id="4d349-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="4d349-119">Se o aplicativo de recebimento precisar acessar os dados após o [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retornar, ele deverá copiar os dados em um buffer local.</span><span class="sxs-lookup"><span data-stu-id="4d349-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="4d349-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d349-120">Examples</span></span>

<span data-ttu-id="4d349-121">Para obter um exemplo, consulte [usando a cópia de dados](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="4d349-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d349-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d349-122">Requirements</span></span>



| <span data-ttu-id="4d349-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d349-123">Requirement</span></span> | <span data-ttu-id="4d349-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4d349-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d349-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d349-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4d349-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d349-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4d349-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d349-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4d349-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4d349-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d349-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4d349-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d349-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d349-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d349-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d349-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d349-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4d349-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d349-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4d349-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="4d349-134">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="4d349-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

