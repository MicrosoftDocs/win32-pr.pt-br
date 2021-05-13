---
description: Contém informações que o Gerenciador de Arquivos usa para adicionar uma cadeia de caracteres de Ajuda para um menu ou item de comando da barra de ferramentas.
title: FMS_HELPSTRING (Wfext.h)
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
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842207"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="1c2d8-103">Estrutura HELPSTRING do FMS \_</span><span class="sxs-lookup"><span data-stu-id="1c2d8-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="1c2d8-104">Contém informações que o Gerenciador de Arquivos usa para adicionar uma cadeia de caracteres de Ajuda para um menu ou item de comando da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="1c2d8-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c2d8-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="1c2d8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1c2d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1c2d8-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="1c2d8-108">Tipo: **INT**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="1c2d8-109">O identificador do item de comando.</span><span class="sxs-lookup"><span data-stu-id="1c2d8-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="1c2d8-110">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="1c2d8-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="1c2d8-112">O identificador da barra de menus.</span><span class="sxs-lookup"><span data-stu-id="1c2d8-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="1c2d8-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="1c2d8-114">Tipo: **\_ \_ wchar \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="1c2d8-115">A cadeia de caracteres terminada em nulo que recebe o texto da Ajuda.</span><span class="sxs-lookup"><span data-stu-id="1c2d8-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c2d8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c2d8-116">Requirements</span></span>



| <span data-ttu-id="1c2d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2d8-117">Requirement</span></span> | <span data-ttu-id="1c2d8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1c2d8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2d8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c2d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2d8-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c2d8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1c2d8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c2d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2d8-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c2d8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c2d8-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1c2d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c2d8-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c2d8-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c2d8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c2d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2d8-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="1c2d8-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="1c2d8-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




