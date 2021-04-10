---
title: Estrutura de DSA_SEC_PAGE_INFO
description: Usado com a planilha do WM \_ ADSPROP \_ \_ criar e o WM \_ DSA \_ sheet \_ criar \_ mensagens de notificação para definir uma folha de propriedades secundária em um snap-in do Active Directory MMC.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Estrutura de DSA_SEC_PAGE_INFO Active Directory
- Ponteiro de estrutura de PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918713"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="5fe9e-105">\_Estrutura de \_ informações da página DSA SEC \_</span><span class="sxs-lookup"><span data-stu-id="5fe9e-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="5fe9e-106">A estrutura de **\_ informações da \_ página \_ DSA SEC** é usada com a folha do [**WM \_ ADSPROP \_ \_ criar**](wm-adsprop-sheet-create.md) e o [**WM \_ DSA \_ sheet \_ criar \_**](wm-dsa-sheet-create-notify.md) mensagens de notificação para definir uma folha de propriedades secundária em um snap-in do Active Directory MMC.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="5fe9e-107">Essa estrutura não está definida em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="5fe9e-108">Para usar essa estrutura, defina-a no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5fe9e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fe9e-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="5fe9e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5fe9e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5fe9e-111">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="5fe9e-112">Contém o identificador de janela do pai da folha de propriedades secundária.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="5fe9e-113">**offsetTitle**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="5fe9e-114">Contém o deslocamento, em bytes, do início da estrutura de **\_ \_ \_ informações da página DSA s** para uma cadeia de caracteres Unicode terminada em nulo que contém o título da folha de propriedades secundária.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="5fe9e-115">**dsObjectNames**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="5fe9e-116">Contém uma estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que define a folha de propriedades secundária.</span><span class="sxs-lookup"><span data-stu-id="5fe9e-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="5fe9e-117">Somente uma folha de propriedades secundária pode ser criada de cada vez, portanto a estrutura **DSOBJECTNAMES** pode conter apenas uma estrutura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="5fe9e-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fe9e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fe9e-118">Requirements</span></span>



| <span data-ttu-id="5fe9e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fe9e-119">Requirement</span></span> | <span data-ttu-id="5fe9e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5fe9e-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5fe9e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fe9e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5fe9e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fe9e-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5fe9e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fe9e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5fe9e-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fe9e-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fe9e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fe9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe9e-126">**criação da planilha do WM \_ ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="5fe9e-127">**\_notificação de \_ criação da folha DSA \_ do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="5fe9e-128">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="5fe9e-129">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="5fe9e-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





