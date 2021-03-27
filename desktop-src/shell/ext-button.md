---
description: Contém informações sobre um botão que uma DLL de extensão do Gerenciador de arquivos está adicionando à barra de ferramentas do Gerenciador de arquivos.
title: Estrutura de EXT_BUTTON (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647028"
---
# <a name="ext_button-structure"></a><span data-ttu-id="6a27a-103">\_Estrutura do botão ext</span><span class="sxs-lookup"><span data-stu-id="6a27a-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="6a27a-104">Contém informações sobre um botão que uma DLL de extensão do Gerenciador de arquivos está adicionando à barra de ferramentas do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6a27a-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a27a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a27a-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="6a27a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6a27a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6a27a-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="6a27a-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="6a27a-108">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a27a-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a27a-109">Um identificador de comando para o botão.</span><span class="sxs-lookup"><span data-stu-id="6a27a-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="6a27a-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="6a27a-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="6a27a-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a27a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a27a-112">O identificador da cadeia de caracteres de ajuda para o botão.</span><span class="sxs-lookup"><span data-stu-id="6a27a-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="6a27a-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="6a27a-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="6a27a-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="6a27a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6a27a-115">O estilo do botão.</span><span class="sxs-lookup"><span data-stu-id="6a27a-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a27a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a27a-116">Requirements</span></span>



| <span data-ttu-id="6a27a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a27a-117">Requirement</span></span> | <span data-ttu-id="6a27a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a27a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a27a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a27a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a27a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a27a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6a27a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a27a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a27a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a27a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a27a-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6a27a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a27a-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a27a-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a27a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a27a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a27a-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="6a27a-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="6a27a-127">**TOOLBARLOAD do FMS \_**</span><span class="sxs-lookup"><span data-stu-id="6a27a-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




