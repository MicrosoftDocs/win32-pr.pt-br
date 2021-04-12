---
description: A \_ estrutura de solicitação de e/s scartar \_ inicia uma estrutura de informações de controle de protocolo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Estrutura de SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296713"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="64c24-103">\_Estrutura de solicitação de e/s scartar \_</span><span class="sxs-lookup"><span data-stu-id="64c24-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="64c24-104">A estrutura de **\_ \_ solicitação de e/s scartar** inicia uma estrutura de informações de controle de protocolo.</span><span class="sxs-lookup"><span data-stu-id="64c24-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="64c24-105">Qualquer informação específica do protocolo segue imediatamente essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="64c24-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="64c24-106">O comprimento total da estrutura deve estar alinhado com o tamanho da palavra da arquitetura de hardware subjacente.</span><span class="sxs-lookup"><span data-stu-id="64c24-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="64c24-107">Por exemplo, no Win32, o comprimento de qualquer informação de PCI deve ser um múltiplo de quatro bytes para que ele se alinhe em um limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64c24-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c24-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64c24-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="64c24-109">Membros</span><span class="sxs-lookup"><span data-stu-id="64c24-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="64c24-110">**dwProtocol**</span><span class="sxs-lookup"><span data-stu-id="64c24-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="64c24-111">Protocolo em uso.</span><span class="sxs-lookup"><span data-stu-id="64c24-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="64c24-112">**cbPciLength**</span><span class="sxs-lookup"><span data-stu-id="64c24-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="64c24-113">Comprimento, em bytes, da estrutura **de \_ \_ solicitação de e/s scartar** , além das informações específicas de PCI a seguir.</span><span class="sxs-lookup"><span data-stu-id="64c24-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64c24-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64c24-114">Requirements</span></span>



| <span data-ttu-id="64c24-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="64c24-115">Requirement</span></span> | <span data-ttu-id="64c24-116">Valor</span><span class="sxs-lookup"><span data-stu-id="64c24-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64c24-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64c24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="64c24-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="64c24-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="64c24-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64c24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="64c24-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64c24-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64c24-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64c24-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="64c24-122"><dt>Winsmcrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="64c24-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c24-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="64c24-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c24-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="64c24-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




