---
description: A \_ estrutura t de escape de recursos do MXDC S0PAGE \_ \_ \_ é uma \_ estrutura t de cabeçalho de escape MXDC \_ \_ concatenada com uma \_ estrutura de \_ \_ f Resource T MXDC XPS S0PAGE \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Estrutura de MXDC_S0PAGE_RESOURCE_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169458"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="293b7-103">\_Estrutura T MXDC S0PAGE de \_ recursos de \_ escape \_</span><span class="sxs-lookup"><span data-stu-id="293b7-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="293b7-104">A **estrutura \_ \_ t de \_ escape \_ de recursos do MXDC S0PAGE** é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ \_ f Resource \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="293b7-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="293b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="293b7-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="293b7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="293b7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="293b7-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="293b7-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="293b7-108">Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como MXDCOP \_ set \_ S0PAGE \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="293b7-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="293b7-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="293b7-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="293b7-110">Uma estrutura [**T do MXDC \_ XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) que representa um recurso, como um arquivo de fonte ou imagem, em uma página de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="293b7-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="293b7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="293b7-111">Remarks</span></span>

<span data-ttu-id="293b7-112">Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **opcode** da estrutura T do [**\_ cabeçalho de \_ escape \_ MXDC**](mxdcescapeheader.md) é **MXDCOP \_ \_ \_ recurso S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="293b7-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="293b7-113">O resultado é um recurso de página a ser enviado para o MXDC.</span><span class="sxs-lookup"><span data-stu-id="293b7-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="293b7-114">Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="293b7-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="293b7-115">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); no entanto, pode haver mais de uma dessas chamadas entre as chamadas para **Startpage** e **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="293b7-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="293b7-116">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **opcode** do **\_ recurso MXDCOP Set \_ S0PAGE \_** para cada recurso na página antes de chamar **ExtEscape** com o **opcode** MXDCOP **\_ set \_ S0PAGE**.  </span><span class="sxs-lookup"><span data-stu-id="293b7-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="293b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293b7-117">Requirements</span></span>



| <span data-ttu-id="293b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="293b7-118">Requirement</span></span> | <span data-ttu-id="293b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="293b7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="293b7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="293b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="293b7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="293b7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="293b7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="293b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="293b7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="293b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="293b7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="293b7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="293b7-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="293b7-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293b7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="293b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293b7-127">Impressão</span><span class="sxs-lookup"><span data-stu-id="293b7-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="293b7-128">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="293b7-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="293b7-129">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="293b7-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="293b7-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="293b7-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="293b7-131">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="293b7-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

