---
description: A \_ estrutura PROVIDOR info \_ 2 acrescenta um provedor de impressão à lista de pedidos do provedor de impressão.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Estrutura de PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810412"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="5dfb3-103">Estrutura de informações de PROVIDOR \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="5dfb3-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="5dfb3-104">A estrutura **PROVIDOR \_ info \_ 2** acrescenta um provedor de impressão à lista de pedidos do provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="5dfb3-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dfb3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dfb3-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="5dfb3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5dfb3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5dfb3-107">**pOrder**</span><span class="sxs-lookup"><span data-stu-id="5dfb3-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="5dfb3-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="5dfb3-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dfb3-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dfb3-109">Remarks</span></span>

<span data-ttu-id="5dfb3-110">Essa estrutura é usada ao chamar [**AddPrintProvidor**](addprintprovidor.md), nível 2, para adicionar o provedor de impressão especificado ao final da lista de pedidos do provedor de impressão.</span><span class="sxs-lookup"><span data-stu-id="5dfb3-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="5dfb3-111">O provedor será usado imediatamente para roteamento se a chamada for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="5dfb3-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dfb3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dfb3-112">Requirements</span></span>



| <span data-ttu-id="5dfb3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dfb3-113">Requirement</span></span> | <span data-ttu-id="5dfb3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5dfb3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dfb3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dfb3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5dfb3-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5dfb3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5dfb3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dfb3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5dfb3-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5dfb3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5dfb3-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5dfb3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dfb3-120"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dfb3-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5dfb3-121">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5dfb3-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5dfb3-122">**\_ PROVIDOR \_ info \_ 2W** (Unicode) e **\_ PROVIDOR \_ info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5dfb3-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5dfb3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dfb3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dfb3-124">Impressão</span><span class="sxs-lookup"><span data-stu-id="5dfb3-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5dfb3-125">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="5dfb3-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="5dfb3-126">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="5dfb3-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




