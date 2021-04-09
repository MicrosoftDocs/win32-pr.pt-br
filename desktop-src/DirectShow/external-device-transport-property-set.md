---
description: Conjunto de propriedades de transporte de dispositivo externo
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propriedades de transporte de dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088805"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="823a7-103">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="823a7-103">External Device Transport Property Set</span></span>

<span data-ttu-id="823a7-104">Esse conjunto de Propriedades controla o transporte de dados de e para um dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="823a7-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="823a7-105">Na maioria dos casos, os aplicativos não devem usar esse conjunto de propriedades diretamente.</span><span class="sxs-lookup"><span data-stu-id="823a7-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="823a7-106">Em vez disso, use a interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="823a7-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="823a7-107">A tabela a seguir lista as propriedades que são relevantes para aplicativos de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="823a7-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="823a7-108">Para obter uma descrição completa desse conjunto de propriedades, consulte o Microsoft Windows Driver Development Kit DDK.</span><span class="sxs-lookup"><span data-stu-id="823a7-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="823a7-109">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="823a7-109">Property Set GUID</span></span> | <span data-ttu-id="823a7-110">transporte de extensão propsetid \_ \_</span><span class="sxs-lookup"><span data-stu-id="823a7-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="823a7-111">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="823a7-111">Property ID</span></span>                                                                           | <span data-ttu-id="823a7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="823a7-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="823a7-113">**KSPROPERTY \_ EXTXPORT \_ ATN \_ Search**</span><span class="sxs-lookup"><span data-stu-id="823a7-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="823a7-114">Pesquisa um número de faixa absoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="823a7-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="823a7-115">**pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="823a7-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="823a7-116">Pesquisa um código de tempo.</span><span class="sxs-lookup"><span data-stu-id="823a7-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="823a7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="823a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="823a7-118">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="823a7-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



