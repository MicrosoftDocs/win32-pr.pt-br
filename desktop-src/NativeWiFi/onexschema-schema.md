---
description: Define elementos de configuração 802.1 X.
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: Esquema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169386"
---
# <a name="onex-schema"></a><span data-ttu-id="04dbf-103">Esquema OneX</span><span class="sxs-lookup"><span data-stu-id="04dbf-103">OneX Schema</span></span>

<span data-ttu-id="04dbf-104">O esquema OneX define elementos de configuração 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="04dbf-104">The OneX Schema defines 802.1X configuration elements.</span></span> <span data-ttu-id="04dbf-105">Todos os elementos de esquema de OneX se aplicam a perfis com e sem fio.</span><span class="sxs-lookup"><span data-stu-id="04dbf-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="04dbf-106">Para obter uma lista de elementos definidos, consulte [elementos de esquema de Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="04dbf-106">For a list of defined elements, see [OneX Schema Elements](onexschema-elements.md).</span></span>

<span data-ttu-id="04dbf-107">O elemento raiz de um perfil 802.1 X é o elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04dbf-107">The root element of an 802.1X profile is the [**OneX**](onexschema-onex-element.md) element.</span></span> <span data-ttu-id="04dbf-108">Cada perfil terá exatamente um elemento raiz.</span><span class="sxs-lookup"><span data-stu-id="04dbf-108">Each profile will have exactly one root element.</span></span> <span data-ttu-id="04dbf-109">O elemento **Onex** está no `https://www.microsoft.com/networking/OneX/v1` namespace.</span><span class="sxs-lookup"><span data-stu-id="04dbf-109">The **OneX** element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="04dbf-110">Para exibir perfis de exemplo para redes sem fio que incluem elementos de configuração do 802.1 X, consulte os exemplos de perfil a seguir:</span><span class="sxs-lookup"><span data-stu-id="04dbf-110">To view sample profiles for wireless networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="04dbf-111">Exemplo de perfil Bootstrap</span><span class="sxs-lookup"><span data-stu-id="04dbf-111">Bootstrap Profile Sample</span></span>](bootstrap-profile-sample.md)
-   [<span data-ttu-id="04dbf-112">Exemplo de perfil FIPS</span><span class="sxs-lookup"><span data-stu-id="04dbf-112">FIPS Profile Sample</span></span>](fips-profile-sample.md)
-   [<span data-ttu-id="04dbf-113">Exemplo de perfil de Sign-On único</span><span class="sxs-lookup"><span data-stu-id="04dbf-113">Single Sign-On Profile Sample</span></span>](single-sign-on-profile-sample.md)
-   [<span data-ttu-id="04dbf-114">Exemplo de perfil de WPA-Enterprise com PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="04dbf-114">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="04dbf-115">Exemplo de perfil de WPA-Enterprise com TLS</span><span class="sxs-lookup"><span data-stu-id="04dbf-115">WPA-Enterprise with TLS Profile Sample</span></span>](wpa-enterprise-with-tls-profile-sample.md)
-   [<span data-ttu-id="04dbf-116">Exemplo de perfil WPA2-Enterprise com PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="04dbf-116">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="04dbf-117">Exemplo de perfil WPA2-Enterprise com TLS</span><span class="sxs-lookup"><span data-stu-id="04dbf-117">WPA2-Enterprise with TLS Profile Sample</span></span>](wpa2-enterprise-with-tls-profile-sample.md)

<span data-ttu-id="04dbf-118">Para exibir perfis de exemplo para redes com fio que incluem elementos de configuração do 802.1 X, consulte os exemplos de perfil a seguir:</span><span class="sxs-lookup"><span data-stu-id="04dbf-118">To view sample profiles for wired networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="04dbf-119">Exemplo de perfil de certificado do computador</span><span class="sxs-lookup"><span data-stu-id="04dbf-119">Machine Certificate Profile Sample</span></span>](machine-certificate-profile-sample.md)
-   [<span data-ttu-id="04dbf-120">Exemplo de perfil de PEAP</span><span class="sxs-lookup"><span data-stu-id="04dbf-120">PEAP Profile Sample</span></span>](peap-profile-sample.md)
-   [<span data-ttu-id="04dbf-121">Perfil de exemplo de certificado de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="04dbf-121">Smart Card Certificate Sample Profile</span></span>](smart-card-certificate-profile-sample.md)

 

 



