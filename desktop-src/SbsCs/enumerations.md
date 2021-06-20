---
description: Saiba mais sobre as enumerações usadas na API de assembly lado a lado, como ASM_CMP_FLAGS e CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Enumerações de assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404739"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="64d10-103">Enumerações de assembly lado a lado</span><span class="sxs-lookup"><span data-stu-id="64d10-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="64d10-104">A API de assembly lado a lado usa as enumerações a seguir.</span><span class="sxs-lookup"><span data-stu-id="64d10-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="64d10-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="64d10-105">Enumeration</span></span>                                                         | <span data-ttu-id="64d10-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="64d10-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64d10-107">**SINALIZADORES \_ CMP DO ASM \_**</span><span class="sxs-lookup"><span data-stu-id="64d10-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="64d10-108">Usado pelo método [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) para especificar quais partes de dois nomes de assembly devem ser comparadas.</span><span class="sxs-lookup"><span data-stu-id="64d10-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="64d10-109">**SINALIZADORES DE \_ EXIBIÇÃO DO ASM \_**</span><span class="sxs-lookup"><span data-stu-id="64d10-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="64d10-110">Usado pelo método [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) para especificar quais partes do nome do assembly lado a lado incluir na representação de cadeia de caracteres do nome.</span><span class="sxs-lookup"><span data-stu-id="64d10-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="64d10-111">**NOME \_ DO ASM**</span><span class="sxs-lookup"><span data-stu-id="64d10-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="64d10-112">IDs de propriedade para os pares nome-valor em um nome de assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="64d10-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="64d10-113">**CRIAR \_ SINALIZADORES \_ OBJ DE \_ NOME \_ ASM**</span><span class="sxs-lookup"><span data-stu-id="64d10-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="64d10-114">Usado pela [**função CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) para especificar o nome do assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="64d10-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



