---
description: A \_ estrutura T do cabeçalho de escape MXDC \_ \_ contém o código da operação para uma chamada para ExtEscape com MXDC \_ escape como o parâmetro nEscape. Ele também fornece os tamanhos dos buffers de entrada e saída.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Estrutura de MXDC_ESCAPE_HEADER_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837144"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="6fdf5-104">\_ \_ Estrutura T do cabeçalho de escape MXDC \_</span><span class="sxs-lookup"><span data-stu-id="6fdf5-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="6fdf5-105">A **estrutura \_ \_ \_ T do cabeçalho de escape MXDC** contém o código da operação para uma chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com [**MXDC \_ escape**](mxdc-escape.md) como o parâmetro *nEscape* .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="6fdf5-106">Ele também fornece os tamanhos dos buffers de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdf5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fdf5-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="6fdf5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6fdf5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fdf5-109">**cbInput**</span><span class="sxs-lookup"><span data-stu-id="6fdf5-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="6fdf5-110">O tamanho do buffer de entrada que será passado para o parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="6fdf5-111">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="6fdf5-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="6fdf5-112">O tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-112">The size of the output buffer.</span></span> <span data-ttu-id="6fdf5-113">Esse é o mesmo valor que o parâmetro *cbOutput* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="6fdf5-114">**opCode**</span><span class="sxs-lookup"><span data-stu-id="6fdf5-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="6fdf5-115">A constante de código que diz ao MXDC o que fazer.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="6fdf5-116">Código de operações</span><span class="sxs-lookup"><span data-stu-id="6fdf5-116">Operations code</span></span>                      | <span data-ttu-id="6fdf5-117">Description</span><span class="sxs-lookup"><span data-stu-id="6fdf5-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdf5-118">MXDCOP \_ obter \_ nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="6fdf5-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="6fdf5-119">Retorna, no parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , o caminho completo do arquivo de saída como uma cadeia de caracteres terminada em zero ou o tamanho dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="6fdf5-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-120">See Remarks.</span></span>                   |
| <span data-ttu-id="6fdf5-121">\_Seq de \_ \_ Doc fixo \_ do MXDCOP PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="6fdf5-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="6fdf5-122">Associa um tíquete de impressão a uma sequência de documento fixa XPS.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="6fdf5-123">\_ \_ Doc fixo do MXDCOP PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="6fdf5-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="6fdf5-124">Associa um tíquete de impressão a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6fdf5-125">\_ \_ página fixa do MXDCOP PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="6fdf5-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="6fdf5-126">Associa um tíquete de impressão a uma página XPS.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="6fdf5-127">MXDCOP \_ set \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="6fdf5-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="6fdf5-128">Envia a marcação XPS da página atual para a saída.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="6fdf5-129">MXDCOP \_ definir \_ \_ recurso S0PAGE</span><span class="sxs-lookup"><span data-stu-id="6fdf5-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="6fdf5-130">Envia um recurso na página, como uma imagem ou fonte, para a saída.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="6fdf5-131">MXDCOP \_ definir \_ \_ modo XPSPASSTHRU</span><span class="sxs-lookup"><span data-stu-id="6fdf5-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="6fdf5-132">Coloca o MXDC em um estado de passagem, permitindo que um aplicativo grave o XPS diretamente no arquivo de saída sem nenhum processamento pelo MXDC.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="6fdf5-133">Um documento inteiro ou até mesmo uma sequência de documento pode ser escrito dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fdf5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fdf5-134">Remarks</span></span>

<span data-ttu-id="6fdf5-135">Antes de chamar [**MXDC \_ escape**](mxdc-escape.md), os \_ aplicativos devem primeiro verificar se o driver é MXDC chamando [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o escape [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="6fdf5-136">Se o driver for o MXDC, a função retornará a cadeia de caracteres terminada em zero " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="6fdf5-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="6fdf5-137">Essa estrutura está sempre no início dos dados passados para a função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) em seu parâmetro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="6fdf5-138">Quando **opcode** é MXDCOP, \_ Get \_ filename:</span><span class="sxs-lookup"><span data-stu-id="6fdf5-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="6fdf5-139">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste apenas na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="6fdf5-140">Obtenha o nome de arquivo de saída chamando [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) duas vezes.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="6fdf5-141">Na primeira vez, passe 4 para o parâmetro *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="6fdf5-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="6fdf5-142">Defina o parâmetro *lpszOutData* para apontar para todos os 4 bytes alocados de memória.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="6fdf5-143">O tamanho do caminho de arquivo totalmente qualificado será retornado no parâmetro *lpszOutData* de **ExtEscape**.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="6fdf5-144">Em seguida, chame a função novamente.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-144">Then call the function again.</span></span> <span data-ttu-id="6fdf5-145">Dessa vez, defina *cbOutput* e *cbInput* como 4 + Data *size*.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="6fdf5-146">O caminho de arquivo totalmente qualificado será retornado em uma estrutura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="6fdf5-147">Quando **opcode** for MXDCOP \_ PrintTicket \_ Fixed \_ doc \_ Seq ou MXDCOP \_ PrintTicket \_ Fixed \_ doc:</span><span class="sxs-lookup"><span data-stu-id="6fdf5-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="6fdf5-148">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada em uma estrutura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="6fdf5-149">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e uma chamada para [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="6fdf5-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="6fdf5-150">Quando **opcode** é uma \_ página fixa do MXDCOP PRINTTICKET \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="6fdf5-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="6fdf5-151">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada em uma estrutura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="6fdf5-152">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="6fdf5-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="6fdf5-153">Quando **opcode** é MXDCOP, \_ defina \_ S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="6fdf5-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="6fdf5-154">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenada em uma estrutura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="6fdf5-155">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="6fdf5-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="6fdf5-156">O aplicativo de chamada é responsável por validar o XML.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="6fdf5-157">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com \_ \_ o recurso MXDCOP Set S0PAGE \_ como **opcode** para cada recurso na página antes de chamá-lo com MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="6fdf5-158">Quando **opcode** é MXDCOP, \_ defina o \_ \_ recurso S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="6fdf5-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="6fdf5-159">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** e em uma estrutura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenada em uma estrutura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="6fdf5-160">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve ocorrer entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), mas pode haver várias chamadas entre as chamadas **Startpage** e **EndPage** .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="6fdf5-161">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com \_ \_ o recurso MXDCOP Set S0PAGE \_ como **opcode** para cada recurso na página antes de chamá-lo com MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="6fdf5-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="6fdf5-162">Quando **opcode** é MXDCOP, \_ defina o \_ \_ modo XPSPASSTHRU:</span><span class="sxs-lookup"><span data-stu-id="6fdf5-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="6fdf5-163">O parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consiste apenas na estrutura T do **\_ \_ cabeçalho de \_ escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="6fdf5-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="6fdf5-164">Essa chamada deve ocorrer antes da chamada para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span><span class="sxs-lookup"><span data-stu-id="6fdf5-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdf5-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fdf5-165">Requirements</span></span>



| <span data-ttu-id="6fdf5-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fdf5-166">Requirement</span></span> | <span data-ttu-id="6fdf5-167">Valor</span><span class="sxs-lookup"><span data-stu-id="6fdf5-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6fdf5-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdf5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdf5-169">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fdf5-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6fdf5-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdf5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdf5-171">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fdf5-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6fdf5-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fdf5-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fdf5-173"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdf5-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdf5-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fdf5-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdf5-175">Impressão</span><span class="sxs-lookup"><span data-stu-id="6fdf5-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6fdf5-176">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="6fdf5-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="6fdf5-177">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fdf5-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6fdf5-178">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="6fdf5-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="6fdf5-179">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="6fdf5-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

