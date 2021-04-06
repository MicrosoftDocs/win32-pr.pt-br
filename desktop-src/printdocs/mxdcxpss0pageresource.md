---
description: A \_ \_ estrutura T do recurso MXDC XPS S0PAGE \_ \_ contém informações sobre um recurso, como uma imagem ou uma fonte, que está associada a uma página de documento XPS e que deve ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Estrutura de MXDC_XPS_S0PAGE_RESOURCE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828765"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="f6857-103">\_Estrutura MXDC XPS \_ S0PAGE \_ Resource \_ T</span><span class="sxs-lookup"><span data-stu-id="f6857-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="f6857-104">A **estrutura \_ \_ T do \_ recurso \_ MXDC XPS S0PAGE** contém informações sobre um recurso, como uma imagem ou uma fonte, que está associada a uma página de documento XPS e que deve ser passada para o arquivo de saída do Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="f6857-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6857-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6857-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="f6857-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f6857-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6857-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="f6857-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="f6857-108">O tamanho total dessa estrutura e o recurso para o qual ela aponta.</span><span class="sxs-lookup"><span data-stu-id="f6857-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="f6857-109">**dwResourceType**</span><span class="sxs-lookup"><span data-stu-id="f6857-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="f6857-110">Um valor do tipo [**\_ \_ \_ enums de página MXDC S0**](mxdcs0pageenums.md) indicando o tipo de recurso, como imagem TIFF ou fonte TrueType.</span><span class="sxs-lookup"><span data-stu-id="f6857-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="f6857-111">**szUri**</span><span class="sxs-lookup"><span data-stu-id="f6857-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="f6857-112">O URI do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6857-112">The URI of the resource.</span></span> <span data-ttu-id="f6857-113">Isso não pode ter mais de 260 bytes.</span><span class="sxs-lookup"><span data-stu-id="f6857-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f6857-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="f6857-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="f6857-115">O tamanho do recurso em bytes.</span><span class="sxs-lookup"><span data-stu-id="f6857-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f6857-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="f6857-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="f6857-117">Os dados do recurso em uma matriz de bytes com tamanho 1 + o tamanho do recurso.</span><span class="sxs-lookup"><span data-stu-id="f6857-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6857-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6857-118">Remarks</span></span>

<span data-ttu-id="f6857-119">Essa estrutura é anexada a uma [**estrutura \_ \_ \_ T do cabeçalho de escape MXDC**](mxdcescapeheader.md) (que tem seu **opcode** definido como **MXDCOP \_ set \_ S0PAGERESOURCE**) para tornar uma estrutura de [**\_ \_ \_ escape \_ t do recurso MXDC S0PAGE**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="f6857-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="f6857-120">A estrutura de **MXDC de \_ \_ \_ escape \_ de recurso S0PAGE** resultante é passada no parâmetro *lpszInData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) que é chamada com o escape de [**\_ escape MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="f6857-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="f6857-121">O efeito é enviar o recurso para o MXDC para conversão e para ser gravado no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f6857-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="f6857-122">A chamada para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve estar entre uma chamada para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e uma chamada para [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); no entanto, pode haver mais de uma dessas chamadas entre as chamadas para **Startpage** e **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="f6857-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="f6857-123">O consumo de streaming será mais eficiente se você chamar [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o **opcode** do **\_ recurso MXDCOP Set \_ S0PAGE \_** para cada recurso na página antes de chamar **ExtEscape** com o **opcode** MXDCOP **\_ set \_ S0PAGE** .</span><span class="sxs-lookup"><span data-stu-id="f6857-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6857-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6857-124">Requirements</span></span>



| <span data-ttu-id="f6857-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6857-125">Requirement</span></span> | <span data-ttu-id="f6857-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f6857-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f6857-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6857-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f6857-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6857-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f6857-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6857-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f6857-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6857-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6857-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6857-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6857-132"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6857-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6857-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6857-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6857-134">Impressão</span><span class="sxs-lookup"><span data-stu-id="f6857-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f6857-135">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f6857-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="f6857-136">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6857-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f6857-137">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="f6857-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="f6857-138">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="f6857-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

