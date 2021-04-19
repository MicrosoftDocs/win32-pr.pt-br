---
description: '\_Constantes personalizadas de localidade \*'
ms.assetid: a41a7f55-8905-47a1-86c3-74ed40b3834c
title: Constantes LOCALE_CUSTOM *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4e02cc672241fd609a5eda975c0e9e13d29908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778574"
---
# <a name="locale_custom-constants"></a><span data-ttu-id="95c4e-103">\_Constantes personalizadas de localidade \*</span><span class="sxs-lookup"><span data-stu-id="95c4e-103">LOCALE\_CUSTOM\* Constants</span></span>

<span data-ttu-id="95c4e-104">Este tópico define as \_ constantes personalizadas de localidade \* usadas pelo NLS para representar as [localidades personalizadas](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="95c4e-104">This topic defines the LOCALE\_CUSTOM\* constants used by NLS to represent [custom locales](custom-locales.md).</span></span>



| <span data-ttu-id="95c4e-105">Valor</span><span class="sxs-lookup"><span data-stu-id="95c4e-105">Value</span></span>                       | <span data-ttu-id="95c4e-106">Significado</span><span class="sxs-lookup"><span data-stu-id="95c4e-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c4e-107">\_padrão personalizado de localidade \_</span><span class="sxs-lookup"><span data-stu-id="95c4e-107">LOCALE\_CUSTOM\_DEFAULT</span></span>     | <span data-ttu-id="95c4e-108">**Windows Vista e posterior:** A localidade personalizada padrão.</span><span class="sxs-lookup"><span data-stu-id="95c4e-108">**Windows Vista and later:** The default custom locale.</span></span> <span data-ttu-id="95c4e-109">Quando uma função NLS deve retornar um identificador de localidade para uma [localidade suplementar](custom-locales.md) para o usuário atual, a função retorna esse valor em vez do [padrão de \_ usuário \_ de localidade](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="95c4e-109">When an NLS function must return a locale identifier for a [supplemental locale](custom-locales.md) for the current user, the function returns this value instead of [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="95c4e-110">O valor do \_ padrão personalizado de localidade \_ é 0x0C00.</span><span class="sxs-lookup"><span data-stu-id="95c4e-110">The value of LOCALE\_CUSTOM\_DEFAULT is 0x0C00.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="95c4e-111">\_ \_ padrão da interface do usuário personalizada de localidade \_</span><span class="sxs-lookup"><span data-stu-id="95c4e-111">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span> | <span data-ttu-id="95c4e-112">**Windows Vista e posterior:** A localidade personalizada padrão para o MUI.</span><span class="sxs-lookup"><span data-stu-id="95c4e-112">**Windows Vista and later:** The default custom locale for MUI.</span></span> <span data-ttu-id="95c4e-113">Os idiomas preferenciais da interface do usuário e os idiomas de interface do usuário preferenciais do sistema podem incluir, no máximo, uma única linguagem implementada por um LIP (Language Interface Pack) e para o qual o identificador de idioma corresponde a uma localidade complementar.</span><span class="sxs-lookup"><span data-stu-id="95c4e-113">The user preferred UI languages and the system preferred UI languages can include at most a single language that is implemented by a Language Interface Pack (LIP) and for which the language identifier corresponds to a supplemental locale.</span></span> <span data-ttu-id="95c4e-114">Se houver tal linguagem em uma lista, a constante será usada para fazer referência a esse idioma em determinados contextos.</span><span class="sxs-lookup"><span data-stu-id="95c4e-114">If there is such a language in a list, the constant is used to refer to that language in certain contexts.</span></span> <span data-ttu-id="95c4e-115">O valor do \_ padrão da interface do usuário personalizada de localidade \_ \_ é 0x1400.</span><span class="sxs-lookup"><span data-stu-id="95c4e-115">The value of LOCALE\_CUSTOM\_UI\_DEFAULT is 0x1400.</span></span>                    |
| <span data-ttu-id="95c4e-116">LOCALIDADE \_ personalizada \_ não especificada</span><span class="sxs-lookup"><span data-stu-id="95c4e-116">LOCALE\_CUSTOM\_UNSPECIFIED</span></span> | <span data-ttu-id="95c4e-117">**Windows Vista e posterior:** Uma localidade personalizada não especificada, usada para identificar todas as localidades complementares, exceto a localidade do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="95c4e-117">**Windows Vista and later:** An unspecified custom locale, used to identify all supplemental locales except the locale for the current user.</span></span> <span data-ttu-id="95c4e-118">As localidades complementares não podem ser diferenciadas umas das outras por seus identificadores de localidade, mas podem ser diferenciadas por seus [nomes de localidade](locale-names.md).</span><span class="sxs-lookup"><span data-stu-id="95c4e-118">Supplemental locales cannot be distinguished from one another by their locale identifiers, but can be distinguished by their [locale names](locale-names.md).</span></span> <span data-ttu-id="95c4e-119">Algumas funções NLS podem retornar essa constante para indicar que elas não podem fornecer um identificador útil para uma localidade específica.</span><span class="sxs-lookup"><span data-stu-id="95c4e-119">Certain NLS functions can return this constant to indicate that they cannot provide a useful identifier for a particular locale.</span></span> <span data-ttu-id="95c4e-120">O valor de local \_ personalizado não \_ especificado é 0x1000.</span><span class="sxs-lookup"><span data-stu-id="95c4e-120">The value of LOCALE\_CUSTOM\_UNSPECIFIED is 0x1000.</span></span> |



 

 

 



