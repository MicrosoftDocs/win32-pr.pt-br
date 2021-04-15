---
description: Especifica a classe do serviço do Agendador de classes de multimídia (MMCSS) para o thread de decodificação.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propriedade AVDecMmcss (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768412"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="b8f3a-103">Propriedade AVDecMmcss</span><span class="sxs-lookup"><span data-stu-id="b8f3a-103">AVDecMmcss property</span></span>

<span data-ttu-id="b8f3a-104">Especifica a classe do serviço do Agendador de classes de multimídia (MMCSS) para o thread de decodificação.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="b8f3a-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8f3a-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b8f3a-106">Data type</span></span>

<span data-ttu-id="b8f3a-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="b8f3a-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b8f3a-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="b8f3a-108">Property GUID</span></span>

<span data-ttu-id="b8f3a-109">**CODECAPI \_ AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="b8f3a-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="b8f3a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b8f3a-110">Property value</span></span>

<span data-ttu-id="b8f3a-111">O valor dessa propriedade é o nome da classe do MMCSS.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f3a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8f3a-112">Remarks</span></span>

<span data-ttu-id="b8f3a-113">O MMCSS permite que os aplicativos garantam que o processamento sensível ao tempo tem acesso prioritário aos recursos da CPU.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="b8f3a-114">Ele funciona elevando threads registrados para prioridades de thread mais altas enquanto reduz periodicamente suas prioridades para gerar tempo para outros processos.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="b8f3a-115">O valor recomendado para decodificadores de áudio é "áudio", e o valor recomendado para decodificadores de vídeo é "reprodução".</span><span class="sxs-lookup"><span data-stu-id="b8f3a-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="b8f3a-116">Se o serviço do MMCSS não estiver disponível ou se a classe do MMCSS especificada não existir, a definição da propriedade não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="b8f3a-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f3a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8f3a-117">Requirements</span></span>



| <span data-ttu-id="b8f3a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8f3a-118">Requirement</span></span> | <span data-ttu-id="b8f3a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b8f3a-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f3a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8f3a-120">Header</span></span><br/> | <dl> <span data-ttu-id="b8f3a-121"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f3a-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f3a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8f3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f3a-123">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="b8f3a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b8f3a-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b8f3a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




