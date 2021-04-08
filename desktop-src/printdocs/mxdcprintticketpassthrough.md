---
description: A \_ estrutura de dados T do MXDC PRINTTICKET \_ \_ contém um tíquete de impressão de documento XPS, que contém configurações de impressora e trabalho de impressão, para passar para o arquivo de saída do conversor de documento XPS da Microsoft (MXDC) sem nenhum processamento.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Estrutura de MXDC_PRINTTICKET_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828310"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="19e77-103">\_Estrutura de \_ T de dados do MXDC PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="19e77-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="19e77-104">A estrutura de **\_ \_ dados \_ T do MXDC PRINTTICKET** contém um TÍQUETE de impressão de documento XPS, que contém configurações de impressora e trabalho de impressão, para passar para o arquivo de saída do conversor de documento XPS da Microsoft (MXDC) sem nenhum processamento.</span><span class="sxs-lookup"><span data-stu-id="19e77-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19e77-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="19e77-106">Membros</span><span class="sxs-lookup"><span data-stu-id="19e77-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="19e77-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="19e77-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="19e77-108">O tamanho do tíquete de impressão em bytes.</span><span class="sxs-lookup"><span data-stu-id="19e77-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="19e77-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="19e77-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="19e77-110">O tíquete de impressão do documento XPS.</span><span class="sxs-lookup"><span data-stu-id="19e77-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19e77-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="19e77-111">Remarks</span></span>

<span data-ttu-id="19e77-112">Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) que tem o membro **opcode** definido como **MXDCOP de \_ \_ \_ página fixa PrintTicket**, **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PRINTTICKET \_ Fixed \_ doc \_ Seq** para fazer uma estrutura de [**escape do MXDC \_ PrintTicket \_ \_**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="19e77-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="19e77-113">A estrutura de **\_ \_ escape \_ T do MXDC PRINTTICKET** é passada para o parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com o escape de [**\_ escape MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="19e77-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="19e77-114">O efeito é gravar o tíquete de impressão no arquivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="19e77-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="19e77-115">Se o **opcode** for definido como **\_ \_ \_ página fixa do MXDCOP PRINTTICKET**, a chamada [**para ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deverá ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="19e77-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="19e77-116">Se o **opcode** estiver definido como **MXDCOP \_ PrintTicket \_ Fixed \_ Doc** ou **MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq**, a chamada para **ExtEscape** deverá ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="19e77-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="19e77-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19e77-117">Requirements</span></span>



| <span data-ttu-id="19e77-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e77-118">Requirement</span></span> | <span data-ttu-id="19e77-119">Valor</span><span class="sxs-lookup"><span data-stu-id="19e77-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="19e77-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19e77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19e77-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19e77-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19e77-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19e77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19e77-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19e77-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="19e77-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19e77-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e77-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="19e77-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e77-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="19e77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e77-127">Impressão</span><span class="sxs-lookup"><span data-stu-id="19e77-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="19e77-128">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="19e77-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="19e77-129">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19e77-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="19e77-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="19e77-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="19e77-131">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="19e77-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

