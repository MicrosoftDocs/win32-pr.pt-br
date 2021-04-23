---
description: Conjunto de propriedades de transporte de dispositivo externo
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propriedades de transporte de dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909214"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="a2b3f-103">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="a2b3f-103">External Device Transport Property Set</span></span>

<span data-ttu-id="a2b3f-104">Esse conjunto de Propriedades controla o transporte de dados de e para um dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="a2b3f-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="a2b3f-105">Na maioria dos casos, os aplicativos não devem usar esse conjunto de propriedades diretamente.</span><span class="sxs-lookup"><span data-stu-id="a2b3f-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="a2b3f-106">Em vez disso, use a interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="a2b3f-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="a2b3f-107">A tabela a seguir lista as propriedades que são relevantes para aplicativos de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="a2b3f-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="a2b3f-108">Para obter uma descrição completa desse conjunto de propriedades, consulte o Microsoft Windows Driver Development Kit DDK.</span><span class="sxs-lookup"><span data-stu-id="a2b3f-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="a2b3f-109">Label</span><span class="sxs-lookup"><span data-stu-id="a2b3f-109">Label</span></span> | <span data-ttu-id="a2b3f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b3f-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="a2b3f-111">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2b3f-111">Property Set GUID</span></span> | <span data-ttu-id="a2b3f-112">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="a2b3f-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="a2b3f-113">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2b3f-113">Property ID</span></span>                                                                           | <span data-ttu-id="a2b3f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2b3f-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="a2b3f-115">**KSPROPERTY \_ EXTXPORT \_ ATN \_ Search**</span><span class="sxs-lookup"><span data-stu-id="a2b3f-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="a2b3f-116">Pesquisa um número de faixa absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="a2b3f-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="a2b3f-117">**pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2b3f-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="a2b3f-118">Pesquisa um código de tempo.</span><span class="sxs-lookup"><span data-stu-id="a2b3f-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a2b3f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2b3f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2b3f-120">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="a2b3f-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



