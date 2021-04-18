---
description: A \_ estrutura t de escape do MXDC PRINTTICKET \_ \_ é uma \_ estrutura t do cabeçalho de escape do MXDC \_ \_ concatenada com uma \_ estrutura de dados t do MXDC PRINTTICKET \_ \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Estrutura de MXDC_PRINTTICKET_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751804"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="76fdf-103">\_ \_ Estrutura T de escape do MXDC PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="76fdf-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="76fdf-104">A **estrutura \_ \_ \_ t de escape do MXDC PRINTTICKET** é uma estrutura [**\_ \_ \_ t do cabeçalho de escape do MXDC**](mxdcescapeheader.md) concatenada com uma estrutura de [**\_ \_ dados \_ t do MXDC PRINTTICKET**](mxdcprintticketpassthrough.md) .</span><span class="sxs-lookup"><span data-stu-id="76fdf-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fdf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76fdf-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="76fdf-106">Membros</span><span class="sxs-lookup"><span data-stu-id="76fdf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="76fdf-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="76fdf-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="76fdf-108">Uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) com seu membro **opcode** definido como página fixa do MXDCOP \_ PrintTicket \_ \_ , \_ documento fixo MXDCOP PrintTicket \_ \_ ou MXDCOP \_ PrintTicket \_ fixo \_ doc \_ Seq.</span><span class="sxs-lookup"><span data-stu-id="76fdf-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="76fdf-109">**printTicketData**</span><span class="sxs-lookup"><span data-stu-id="76fdf-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="76fdf-110">Uma estrutura de [**\_ \_ dados \_ de MXDC PRINTTICKET**](mxdcprintticketpassthrough.md) que contém o tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="76fdf-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76fdf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="76fdf-111">Remarks</span></span>

<span data-ttu-id="76fdf-112">Essa estrutura é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando essa função é chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e o membro **de opcode** da estrutura [**\_ \_ \_ T do cabeçalho de escape MXDC**](mxdcescapeheader.md) é a **\_ \_ \_ página fixa MXDCOP PrintTicket**, **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq**.</span><span class="sxs-lookup"><span data-stu-id="76fdf-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="76fdf-113">O resultado é gravar o tíquete de impressão no arquivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="76fdf-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="76fdf-114">Aloque memória para o escape, conforme mostrado abaixo, defina os campos conforme necessário e, em seguida, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="76fdf-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="76fdf-115">Se o **opcode** for definido como **\_ \_ \_ página fixa do MXDCOP PRINTTICKET**, a chamada [**para ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deverá ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="76fdf-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="76fdf-116">Se o **opcode** estiver definido como **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq**, a chamada para **ExtEscape** deverá ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="76fdf-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="76fdf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76fdf-117">Requirements</span></span>



| <span data-ttu-id="76fdf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76fdf-118">Requirement</span></span> | <span data-ttu-id="76fdf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="76fdf-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76fdf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76fdf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76fdf-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76fdf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76fdf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76fdf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76fdf-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76fdf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="76fdf-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76fdf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76fdf-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="76fdf-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fdf-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="76fdf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fdf-127">Impressão</span><span class="sxs-lookup"><span data-stu-id="76fdf-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="76fdf-128">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="76fdf-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="76fdf-129">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76fdf-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="76fdf-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="76fdf-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="76fdf-131">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="76fdf-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

