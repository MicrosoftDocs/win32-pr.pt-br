---
title: Constantes de GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes especifique a posição do caractere a ser retornada com base nas coordenadas da tela do ponto em relação a uma caixa delimitadora de caracteres.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454845"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="5e258-103">\_ \* Constantes GXFPF</span><span class="sxs-lookup"><span data-stu-id="5e258-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="5e258-104">\_ \* As constantes GXFPF especificam a posição do caractere a ser retornada com base nas coordenadas da tela do ponto em relação a uma caixa delimitadora de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e258-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="5e258-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="5e258-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="5e258-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e258-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="5e258-107"><dt>**GXFPF \_ ROUND \_ mais próximo**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5e258-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="5e258-108">Se as coordenadas da tela do ponto estiverem contidas em uma caixa delimitadora de caracteres, a posição do caractere retornada será a borda delimitadora mais próxima das coordenadas da tela do ponto.</span><span class="sxs-lookup"><span data-stu-id="5e258-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="5e258-109"><dt>**GXFPF \_ A mais próxima**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5e258-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="5e258-110">Se as coordenadas da tela do ponto não estiverem contidas em uma caixa delimitadora de caracteres, a posição do caractere mais próxima será retornada.</span><span class="sxs-lookup"><span data-stu-id="5e258-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="5e258-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e258-111">Remarks</span></span>

<span data-ttu-id="5e258-112">Os parâmetros *dwFlags* dos métodos [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) e [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usam essas constantes.</span><span class="sxs-lookup"><span data-stu-id="5e258-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e258-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e258-113">Requirements</span></span>



| <span data-ttu-id="5e258-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e258-114">Requirement</span></span> | <span data-ttu-id="5e258-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5e258-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e258-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e258-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e258-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e258-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e258-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e258-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e258-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e258-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e258-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5e258-120">Redistributable</span></span><br/>          | <span data-ttu-id="5e258-121">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5e258-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="5e258-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e258-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e258-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e258-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e258-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="5e258-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e258-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e258-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e258-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e258-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e258-127">ITextStoreACP:: GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="5e258-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="5e258-128">ITfContextOwner::GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="5e258-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





