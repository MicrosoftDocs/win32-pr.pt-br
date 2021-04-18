---
description: Especifica o nível médio de volume de conteúdo de áudio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Propriedade MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756330"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="31e6b-103">\_Propriedade MFPKEY WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="31e6b-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="31e6b-104">Especifica o nível médio de volume de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="31e6b-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31e6b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="31e6b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="31e6b-106">g \_ wszWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="31e6b-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="31e6b-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="31e6b-107">Data Type</span></span>

<span data-ttu-id="31e6b-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="31e6b-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="31e6b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="31e6b-109">Remarks</span></span>

<span data-ttu-id="31e6b-110">Você pode obter esse valor do codificador depois que o conteúdo é processado.</span><span class="sxs-lookup"><span data-stu-id="31e6b-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="31e6b-111">Esse valor também pode ser definido no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.</span><span class="sxs-lookup"><span data-stu-id="31e6b-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="31e6b-112">Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da Web [recursos de codec do Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="31e6b-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="31e6b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31e6b-113">Requirements</span></span>



| <span data-ttu-id="31e6b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e6b-114">Requirement</span></span> | <span data-ttu-id="31e6b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="31e6b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e6b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e6b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31e6b-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31e6b-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31e6b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31e6b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31e6b-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31e6b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31e6b-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31e6b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e6b-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e6b-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e6b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="31e6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e6b-123">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31e6b-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
