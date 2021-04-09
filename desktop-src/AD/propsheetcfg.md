---
title: Estrutura PROPSHEETCFG
description: Usado para conter dados de configuração da folha de propriedades.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory estrutura PROPSHEETCFG
- Active Directory de ponteiro de estrutura de PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009404"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="8031b-105">Estrutura PROPSHEETCFG</span><span class="sxs-lookup"><span data-stu-id="8031b-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="8031b-106">A estrutura **PROPSHEETCFG** é usada para conter dados de configuração da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8031b-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="8031b-107">Essa estrutura está contida no formato de área de transferência [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="8031b-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="8031b-108">Essa estrutura não está definida em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="8031b-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="8031b-109">Para usar essa estrutura, você mesmo deve defini-la no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="8031b-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8031b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8031b-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="8031b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="8031b-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="8031b-112">**lNotifyHandle**</span><span class="sxs-lookup"><span data-stu-id="8031b-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="8031b-113">Contém o identificador de notificação.</span><span class="sxs-lookup"><span data-stu-id="8031b-113">Contains the notification handle.</span></span> <span data-ttu-id="8031b-114">Isso é idêntico ao identificador passado para o parâmetro *Handle* no método [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8031b-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="8031b-115">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="8031b-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="8031b-116">Contém o identificador de janela da folha de propriedades pai.</span><span class="sxs-lookup"><span data-stu-id="8031b-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="8031b-117">**hwndHidden**</span><span class="sxs-lookup"><span data-stu-id="8031b-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="8031b-118">Contém o identificador da janela oculta.</span><span class="sxs-lookup"><span data-stu-id="8031b-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="8031b-119">**wParamSheetClose**</span><span class="sxs-lookup"><span data-stu-id="8031b-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="8031b-120">Contém um valor de 32 bits definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8031b-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="8031b-121">Esse valor é passado de volta para o aplicativo no *wParam* da mensagem [**de \_ \_ notificação de \_ fechamento \_ da folha DSA do WM**](wm-dsa-sheet-close-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8031b-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8031b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8031b-122">Requirements</span></span>



| <span data-ttu-id="8031b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8031b-123">Requirement</span></span> | <span data-ttu-id="8031b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8031b-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8031b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8031b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8031b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8031b-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8031b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8031b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8031b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8031b-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8031b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8031b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8031b-130">**CFSTR \_ DS \_ PROPSHEETCONFIG**</span><span class="sxs-lookup"><span data-stu-id="8031b-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="8031b-131">**\_notificação de \_ fechamento da folha DSA \_ do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8031b-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

