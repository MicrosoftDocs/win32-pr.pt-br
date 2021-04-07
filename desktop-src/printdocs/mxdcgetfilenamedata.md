---
description: A \_ estrutura MXDC get \_ filename \_ Data \_ T contém o caminho completo e o nome do arquivo de um arquivo de saída do conversor de documento XPS da Microsoft (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Estrutura de MXDC_GET_FILENAME_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828311"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="32ced-103">MXDC \_ obter \_ nome de arquivo \_ Data \_ T estrutura</span><span class="sxs-lookup"><span data-stu-id="32ced-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="32ced-104">A estrutura **MXDC \_ Get \_ filename \_ Data \_ T** contém o caminho completo e o nome do arquivo de um arquivo de saída do conversor de documento XPS da Microsoft (MXDC).</span><span class="sxs-lookup"><span data-stu-id="32ced-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ced-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32ced-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="32ced-106">Membros</span><span class="sxs-lookup"><span data-stu-id="32ced-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="32ced-107">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="32ced-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="32ced-108">O tamanho do buffer de saída, **wszData**.</span><span class="sxs-lookup"><span data-stu-id="32ced-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="32ced-109">**wszData**</span><span class="sxs-lookup"><span data-stu-id="32ced-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="32ced-110">O caminho totalmente qualificado e o nome de arquivo do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="32ced-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32ced-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ced-111">Remarks</span></span>

<span data-ttu-id="32ced-112">Essa estrutura é retornada por [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando chamada com o escape de [**escape \_ MXDC**](mxdc-escape.md) e a estrutura [**\_ T de \_ cabeçalho \_ de escape MXDC**](mxdcescapeheader.md) que é passada no parâmetro *lpszInData* tem seu **opcode** definido como **MXDCOP \_ Get \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="32ced-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ced-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32ced-113">Requirements</span></span>



| <span data-ttu-id="32ced-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ced-114">Requirement</span></span> | <span data-ttu-id="32ced-115">Valor</span><span class="sxs-lookup"><span data-stu-id="32ced-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="32ced-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ced-116">Minimum supported client</span></span><br/> | <span data-ttu-id="32ced-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32ced-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32ced-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32ced-118">Minimum supported server</span></span><br/> | <span data-ttu-id="32ced-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32ced-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32ced-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32ced-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ced-121"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ced-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ced-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="32ced-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ced-123">Impressão</span><span class="sxs-lookup"><span data-stu-id="32ced-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="32ced-124">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="32ced-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="32ced-125">[Funções de escape de impressora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32ced-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="32ced-126">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="32ced-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="32ced-127">**MXDC \_ escape**</span><span class="sxs-lookup"><span data-stu-id="32ced-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

