---
description: Especifica o número máximo de imagens de um cabeçalho de grupo de imagens (GOP) para o próximo cabeçalho GOP.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propriedade AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010026"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="fff54-103">Propriedade AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="fff54-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="fff54-104">Especifica o número máximo de imagens de um cabeçalho de grupo de imagens (GOP) para o próximo cabeçalho GOP.</span><span class="sxs-lookup"><span data-stu-id="fff54-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="fff54-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fff54-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fff54-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fff54-106">Data type</span></span>

<span data-ttu-id="fff54-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fff54-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fff54-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="fff54-108">Property GUID</span></span>

<span data-ttu-id="fff54-109">**CODECAPI \_ AVEncMPVGOPSize**</span><span class="sxs-lookup"><span data-stu-id="fff54-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="fff54-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fff54-110">Property value</span></span>

<span data-ttu-id="fff54-111">Os codificadores podem implementar essa propriedade como um conjunto enumerado ou como um intervalo linear.</span><span class="sxs-lookup"><span data-stu-id="fff54-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="fff54-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fff54-112">Remarks</span></span>

<span data-ttu-id="fff54-113">Defina essa propriedade antes de iniciar uma gravação.</span><span class="sxs-lookup"><span data-stu-id="fff54-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="fff54-114">**Aplica-se ao Windows 8:** O tamanho de GOP codificado deve ser menor ou igual ao número especificado por meio dessa propriedade, a fim de manter o mesmo padrão de quadro B definido por [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) em toda a GOP ou devido à alteração de cena.</span><span class="sxs-lookup"><span data-stu-id="fff54-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="fff54-115">Por exemplo, quando o número de quadros B em um GOP é especificado como 2 e o tamanho de GOP é 11, o codificador deve produzir o tamanho de GOP de 10 quadros ou menos.</span><span class="sxs-lookup"><span data-stu-id="fff54-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="fff54-116">Quando a alteração de cena ocorre no meio de um GOP, o codificador também pode inserir o quadro-chave e produzir GOP menores.</span><span class="sxs-lookup"><span data-stu-id="fff54-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="fff54-117">O tamanho 0 do GOP é dependente do codificador e os codificadores podem escolher diferentes tamanhos de GOP com base em sua implementação/qualidade/desempenho.</span><span class="sxs-lookup"><span data-stu-id="fff54-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="fff54-118">Os codificadores devem respeitar o tamanho do GOP e truncar os quadros B nesse caso.</span><span class="sxs-lookup"><span data-stu-id="fff54-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff54-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fff54-119">Requirements</span></span>



| <span data-ttu-id="fff54-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff54-120">Requirement</span></span> | <span data-ttu-id="fff54-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fff54-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fff54-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fff54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fff54-123">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fff54-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fff54-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fff54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fff54-125">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fff54-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fff54-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fff54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fff54-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fff54-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff54-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fff54-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff54-129">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="fff54-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fff54-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fff54-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




