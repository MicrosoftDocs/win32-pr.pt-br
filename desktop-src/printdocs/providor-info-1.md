---
description: A \_ estrutura info \_ 1 do PROVIDOR identifica um provedor de impressão.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Estrutura de PROVIDOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297146"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="f8e4c-103">Estrutura de informações de PROVIDOR \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8e4c-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="f8e4c-104">A **estrutura \_ info \_ 1 do PROVIDOR** identifica um provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="f8e4c-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8e4c-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="f8e4c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f8e4c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8e4c-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="f8e4c-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="f8e4c-108">Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="f8e4c-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="f8e4c-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f8e4c-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="f8e4c-110">Ponteiro para uma cadeia de caracteres de ambiente terminada em nulo que especifica o ambiente no qual a DLL (biblioteca de vínculo dinâmico) do provedor foi projetada para ser executada.</span><span class="sxs-lookup"><span data-stu-id="f8e4c-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="f8e4c-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="f8e4c-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="f8e4c-112">Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do Provider. dll.</span><span class="sxs-lookup"><span data-stu-id="f8e4c-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8e4c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e4c-113">Requirements</span></span>



| <span data-ttu-id="f8e4c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e4c-114">Requirement</span></span> | <span data-ttu-id="f8e4c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f8e4c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e4c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e4c-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8e4c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8e4c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e4c-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8e4c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8e4c-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8e4c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e4c-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8e4c-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f8e4c-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f8e4c-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8e4c-123">**\_ PROVIDOR \_ info \_ 1W** (Unicode) e **\_ PROVIDOR \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8e4c-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f8e4c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8e4c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e4c-125">Impressão</span><span class="sxs-lookup"><span data-stu-id="f8e4c-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f8e4c-126">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f8e4c-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f8e4c-127">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="f8e4c-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




