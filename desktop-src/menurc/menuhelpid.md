---
title: Estrutura MENUHELPID
description: Contém os dados finais gravados no \_ recurso de menu RT para um menu ou submenu se o membro resInfo da estrutura POPUPMENUITEM for definido como \_ Popup mfr.
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- Menus de estrutura MENUHELPID e outros recursos
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750884"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="abd50-104">Estrutura MENUHELPID</span><span class="sxs-lookup"><span data-stu-id="abd50-104">MENUHELPID structure</span></span>

<span data-ttu-id="abd50-105">Contém os dados finais gravados no recurso de [**\_ menu RT**](/windows/desktop/menurc/resource-types) para um menu ou submenu se o membro **resInfo** da estrutura [**POPUPMENUITEM**](popupmenuitem.md) for definido como **\_ Popup mfr**.</span><span class="sxs-lookup"><span data-stu-id="abd50-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="abd50-106">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="abd50-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd50-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abd50-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="abd50-108">Membros</span><span class="sxs-lookup"><span data-stu-id="abd50-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="abd50-109">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="abd50-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="abd50-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="abd50-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="abd50-111">O identificador usado para identificar o menu durante o processamento da [**\_ ajuda do WM**](/windows/desktop/shell/wm-help) .</span><span class="sxs-lookup"><span data-stu-id="abd50-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abd50-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abd50-112">Requirements</span></span>



| <span data-ttu-id="abd50-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd50-113">Requirement</span></span> | <span data-ttu-id="abd50-114">Valor</span><span class="sxs-lookup"><span data-stu-id="abd50-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="abd50-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abd50-115">Minimum supported client</span></span><br/> | <span data-ttu-id="abd50-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="abd50-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="abd50-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abd50-117">Minimum supported server</span></span><br/> | <span data-ttu-id="abd50-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="abd50-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="abd50-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="abd50-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="abd50-120">**Referência**</span><span class="sxs-lookup"><span data-stu-id="abd50-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abd50-121">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="abd50-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="abd50-122">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="abd50-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="abd50-123">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="abd50-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="abd50-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="abd50-124">Resources</span></span>](resources.md)
</dt> </dl>

 

