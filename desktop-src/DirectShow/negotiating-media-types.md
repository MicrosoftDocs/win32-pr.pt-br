---
description: Negociando tipos de mídia
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negociando tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105792647"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="25b28-103">Negociando tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="25b28-103">Negotiating Media Types</span></span>

<span data-ttu-id="25b28-104">Quando o Gerenciador de gráfico de filtro chama o método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , ele tem várias opções para especificar um tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="25b28-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="25b28-105">**Tipo completo:** Se o tipo de mídia for totalmente especificado, os Pins tentarão se conectar com esse tipo.</span><span class="sxs-lookup"><span data-stu-id="25b28-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="25b28-106">Se não puderem, a tentativa de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="25b28-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="25b28-107">**Tipo de mídia parcial:** Um tipo de mídia será *parcial* se o tipo de tipo principal, subtipo ou formato for GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="25b28-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="25b28-108">O valor GUID \_ NULL age como um "curinga", indicando que qualquer valor é aceitável.</span><span class="sxs-lookup"><span data-stu-id="25b28-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="25b28-109">Os Pins negociam um tipo que é consistente com o tipo parcial.</span><span class="sxs-lookup"><span data-stu-id="25b28-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="25b28-110">**Nenhum tipo de mídia:** Se o Gerenciador de gráfico de filtro passar um ponteiro **nulo** , os Pins poderão concordar com qualquer tipo de mídia aceitável para ambos os Pins.</span><span class="sxs-lookup"><span data-stu-id="25b28-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="25b28-111">Se os PINs se conectarem, a conexão sempre terá um tipo de mídia completo.</span><span class="sxs-lookup"><span data-stu-id="25b28-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="25b28-112">A finalidade do tipo de mídia fornecido pelo Gerenciador de gráficos de filtro é limitar os possíveis tipos de conexão.</span><span class="sxs-lookup"><span data-stu-id="25b28-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="25b28-113">Durante o processo de negociação, o PIN de saída propõe um tipo de mídia chamando o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="25b28-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="25b28-114">O PIN de entrada pode aceitar ou rejeitar o tipo proposto.</span><span class="sxs-lookup"><span data-stu-id="25b28-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="25b28-115">Esse processo se repete até que o PIN de entrada aceite um tipo, ou que o pino de saída fique sem tipos e a conexão falhe.</span><span class="sxs-lookup"><span data-stu-id="25b28-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="25b28-116">Como um pino de saída seleciona os tipos de mídia a serem propordos depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="25b28-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="25b28-117">Nas classes base do DirectShow, o pino de saída chama [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="25b28-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="25b28-118">Esse método retorna um enumerador que enumera os tipos de mídia preferenciais do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="25b28-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="25b28-119">Falhando, o PIN de saída enumera seus próprios tipos preferenciais.</span><span class="sxs-lookup"><span data-stu-id="25b28-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="25b28-120">**Trabalhando com tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="25b28-120">**Working with Media Types**</span></span>

<span data-ttu-id="25b28-121">Em qualquer função que recebe um parâmetro de **\_ \_ tipo de mídia am** , sempre valide os valores de **cbFormat** e **formatType** antes de desreferenciar o membro **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="25b28-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="25b28-122">O código a seguir está incorreto:</span><span class="sxs-lookup"><span data-stu-id="25b28-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="25b28-123">O código a seguir está correto:</span><span class="sxs-lookup"><span data-stu-id="25b28-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



