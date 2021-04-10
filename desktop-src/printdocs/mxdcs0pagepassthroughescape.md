---
description: A \_ \_ estrutura t de escape de passagem MXDC S0PAGE \_ \_ é uma \_ estrutura t de cabeçalho de escape MXDC \_ \_ concatenada com uma \_ estrutura de \_ f Data T MXDC S0PAGE \_ .
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Estrutura de MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296946"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="2b056-103">\_ \_ \_ Estrutura T de escape de passagem MXDC S0PAGE \_</span><span class="sxs-lookup"><span data-stu-id="2b056-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="2b056-104">A **estrutura \_ \_ t de \_ escape \_ de passagem MXDC S0PAGE** é uma estrutura [**\_ \_ \_ t de cabeçalho de escape MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ f Data \_ T MXDC S0PAGE**](mxdcs0pagedata.md) .</span><span class="sxs-lookup"><span data-stu-id="2b056-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b056-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b056-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="2b056-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2b056-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b056-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="2b056-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="2b056-108">Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2b056-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="2b056-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="2b056-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="2b056-110">Uma estrutura [**MxdcS0PageData**](mxdcs0pagedata.md) que representa uma página de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2b056-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b056-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b056-111">Remarks</span></span>

<span data-ttu-id="2b056-112">Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **opcode** da estrutura [**T do \_ \_ cabeçalho de \_ escape MXDC**](mxdcescapeheader.md) é **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2b056-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="2b056-113">O resultado é que o conversor de documento XML da Microsoft (MXDC) passa a página para a impressora sem processá-la.</span><span class="sxs-lookup"><span data-stu-id="2b056-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="2b056-114">Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="2b056-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="2b056-115">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="2b056-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="2b056-116">O aplicativo de chamada é responsável por validar o XML da página do documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2b056-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="2b056-117">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **\_ recurso MXDCOP Set \_ \_ S0PAGE** como **opcode** para cada recurso na página antes de chamá-lo com **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2b056-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b056-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b056-118">Requirements</span></span>



| <span data-ttu-id="2b056-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b056-119">Requirement</span></span> | <span data-ttu-id="2b056-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2b056-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2b056-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b056-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b056-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b056-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b056-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b056-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b056-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b056-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b056-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b056-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b056-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b056-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b056-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b056-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b056-128">Impressão</span><span class="sxs-lookup"><span data-stu-id="2b056-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2b056-129">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="2b056-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="2b056-130">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2b056-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2b056-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="2b056-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="2b056-132">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="2b056-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

