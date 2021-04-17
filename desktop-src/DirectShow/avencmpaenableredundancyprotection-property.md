---
description: Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriedade AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749274"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="c93d9-104">Propriedade AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="c93d9-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="c93d9-105">Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro.</span><span class="sxs-lookup"><span data-stu-id="c93d9-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="c93d9-106">Essa propriedade se aplica a codificadores de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="c93d9-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="c93d9-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c93d9-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c93d9-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c93d9-108">Data type</span></span>

<span data-ttu-id="c93d9-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="c93d9-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c93d9-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c93d9-110">Property GUID</span></span>

<span data-ttu-id="c93d9-111">**CODECAPI \_ AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="c93d9-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="c93d9-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c93d9-112">Property value</span></span>

<span data-ttu-id="c93d9-113">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c93d9-113">This property can have the following values.</span></span>



| <span data-ttu-id="c93d9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c93d9-114">Value</span></span>          | <span data-ttu-id="c93d9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c93d9-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="c93d9-116">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="c93d9-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="c93d9-117">Não adicione uma soma de verificação de CRC.</span><span class="sxs-lookup"><span data-stu-id="c93d9-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="c93d9-118">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="c93d9-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="c93d9-119">Adicione uma soma de verificação de CRC.</span><span class="sxs-lookup"><span data-stu-id="c93d9-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="c93d9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c93d9-120">Requirements</span></span>



| <span data-ttu-id="c93d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c93d9-121">Requirement</span></span> | <span data-ttu-id="c93d9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c93d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c93d9-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c93d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c93d9-124">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c93d9-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c93d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c93d9-126">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c93d9-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c93d9-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c93d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c93d9-128"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93d9-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93d9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c93d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93d9-130">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="c93d9-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c93d9-131">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c93d9-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




