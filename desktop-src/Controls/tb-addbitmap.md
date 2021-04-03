---
title: Mensagem de TB_ADDBITMAP (commctrl. h)
description: Adiciona uma ou mais imagens à lista de imagens de botão disponíveis para uma barra de ferramentas.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Controles de TB_ADDBITMAP de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645267"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="fe0dc-104">\_Mensagem de ADDBITMAP TB</span><span class="sxs-lookup"><span data-stu-id="fe0dc-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="fe0dc-105">Adiciona uma ou mais imagens à lista de imagens de botão disponíveis para uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe0dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe0dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe0dc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0dc-108">Número de imagens de botão no bitmap.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="fe0dc-109">Se *lParam* especificar um bitmap definido pelo sistema, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="fe0dc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe0dc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0dc-111">Ponteiro para uma estrutura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) que contém o identificador de um recurso de bitmap e o identificador para a instância de módulo com o arquivo executável que contém o recurso de bitmap.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0dc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe0dc-112">Return value</span></span>

<span data-ttu-id="fe0dc-113">Retorna o índice da primeira nova imagem, se for bem-sucedido, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0dc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe0dc-114">Remarks</span></span>

<span data-ttu-id="fe0dc-115">Se a barra de ferramentas foi criada usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , você deve enviar a mensagem [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) para a barra de ferramentas antes de enviar **TB \_ AddBitmap**.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="fe0dc-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe0dc-116">Examples</span></span>

<span data-ttu-id="fe0dc-117">O exemplo a seguir cria um bitmap de um recurso (IDB \_ Bitmap1), mapeia a cor do plano de fundo (preto, neste caso) para a cor de face do botão do sistema e o adiciona à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="fe0dc-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="fe0dc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe0dc-118">Requirements</span></span>



| <span data-ttu-id="fe0dc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0dc-119">Requirement</span></span> | <span data-ttu-id="fe0dc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fe0dc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0dc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0dc-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe0dc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe0dc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0dc-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe0dc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe0dc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe0dc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0dc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0dc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

