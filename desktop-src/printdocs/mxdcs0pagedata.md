---
description: A \_ estrutura de T de dados MXDC S0PAGE \_ \_ contém uma página de documento XPS a ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC) sem nenhum processamento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Estrutura de MXDC_S0PAGE_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662569"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="daf05-103">\_Estrutura de \_ T de dados MXDC S0PAGE \_</span><span class="sxs-lookup"><span data-stu-id="daf05-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="daf05-104">A estrutura de **\_ T de \_ dados \_ MXDC S0PAGE** contém uma página de documento XPS a ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC) sem nenhum processamento.</span><span class="sxs-lookup"><span data-stu-id="daf05-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daf05-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="daf05-106">Membros</span><span class="sxs-lookup"><span data-stu-id="daf05-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="daf05-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="daf05-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="daf05-108">O tamanho do buffer de saída, **bData**.</span><span class="sxs-lookup"><span data-stu-id="daf05-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="daf05-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="daf05-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="daf05-110">A página do documento XPS.</span><span class="sxs-lookup"><span data-stu-id="daf05-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daf05-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf05-111">Remarks</span></span>

<span data-ttu-id="daf05-112">Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T de cabeçalho de escape MXDC**](mxdcescapeheader.md) (que tem seu **opcode** definido como MXDCOP \_ set \_ S0PAGE) para fazer uma estrutura t de [**passagem de S0PAGE de MXDC de \_ \_ \_ saída \_**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="daf05-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="daf05-113">Essa estrutura é passada para o parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando ela é chamada com [**MXDC \_ escape**](mxdc-escape.md) como o escape.</span><span class="sxs-lookup"><span data-stu-id="daf05-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="daf05-114">O resultado é que o MXDC passa a página para a saída sem processá-la.</span><span class="sxs-lookup"><span data-stu-id="daf05-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="daf05-115">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="daf05-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="daf05-116">O aplicativo de chamada é responsável por validar o XML da página do documento XPS.</span><span class="sxs-lookup"><span data-stu-id="daf05-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="daf05-117">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **\_ recurso MXDCOP Set \_ \_ S0PAGE** como **opcode** para cada recurso na página antes de chamá-lo com **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="daf05-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf05-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daf05-118">Requirements</span></span>



| <span data-ttu-id="daf05-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf05-119">Requirement</span></span> | <span data-ttu-id="daf05-120">Valor</span><span class="sxs-lookup"><span data-stu-id="daf05-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="daf05-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="daf05-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="daf05-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="daf05-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="daf05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="daf05-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="daf05-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="daf05-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="daf05-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="daf05-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf05-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf05-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="daf05-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf05-128">Impressão</span><span class="sxs-lookup"><span data-stu-id="daf05-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="daf05-129">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="daf05-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="daf05-130">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="daf05-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="daf05-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="daf05-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="daf05-132">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="daf05-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

