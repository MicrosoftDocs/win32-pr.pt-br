---
description: Contém informações que o Gerenciador de arquivos usa para adicionar uma cadeia de caracteres de ajuda para um menu ou item de comando de barra de ferramentas.
title: Estrutura de FMS_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988998"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="06d9e-103">\_Estrutura HelpString do FMS</span><span class="sxs-lookup"><span data-stu-id="06d9e-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="06d9e-104">Contém informações que o Gerenciador de arquivos usa para adicionar uma cadeia de caracteres de ajuda para um menu ou item de comando de barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="06d9e-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d9e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06d9e-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="06d9e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="06d9e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06d9e-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="06d9e-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="06d9e-108">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="06d9e-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="06d9e-109">O identificador do item de comando.</span><span class="sxs-lookup"><span data-stu-id="06d9e-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="06d9e-110">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="06d9e-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="06d9e-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="06d9e-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="06d9e-112">O identificador da barra de menus.</span><span class="sxs-lookup"><span data-stu-id="06d9e-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="06d9e-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="06d9e-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="06d9e-114">Tipo: **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="06d9e-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="06d9e-115">A cadeia de caracteres terminada em nulo que recebe o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="06d9e-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06d9e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06d9e-116">Requirements</span></span>



| <span data-ttu-id="06d9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="06d9e-117">Requirement</span></span> | <span data-ttu-id="06d9e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="06d9e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06d9e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06d9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="06d9e-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06d9e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="06d9e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06d9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="06d9e-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06d9e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="06d9e-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06d9e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="06d9e-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d9e-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06d9e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="06d9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d9e-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="06d9e-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="06d9e-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="06d9e-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




