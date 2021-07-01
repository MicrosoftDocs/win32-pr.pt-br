---
description: A chave do Registro EUDCCodeRange define intervalos de código euDC (caractere definido pelo usuário final) para várias páginas de código (conjuntos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120671"
---
# <a name="eudccoderange"></a><span data-ttu-id="d59d9-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="d59d9-103">EUDCCodeRange</span></span>

<span data-ttu-id="d59d9-104">A chave do Registro EUDCCodeRange define intervalos de código [euDC (caractere](end-user-defined-characters.md) definido pelo usuário final) para várias páginas de código (conjuntos de caracteres).</span><span class="sxs-lookup"><span data-stu-id="d59d9-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="d59d9-105">Ele é usado apenas por ferramentas que criam EUDCs e não é de interesse direto para usuários do EUDC.</span><span class="sxs-lookup"><span data-stu-id="d59d9-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="d59d9-106">Essa chave do Registro tem o seguinte local do Registro:</span><span class="sxs-lookup"><span data-stu-id="d59d9-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="d59d9-107">HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="d59d9-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="d59d9-108">O formato é:</span><span class="sxs-lookup"><span data-stu-id="d59d9-108">The format is:</span></span>

<span data-ttu-id="d59d9-109">EUDCCodeRange CodePage=FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="d59d9-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="d59d9-110">em que:</span><span class="sxs-lookup"><span data-stu-id="d59d9-110">where:</span></span>



| <span data-ttu-id="d59d9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d59d9-111">Value</span></span>         | <span data-ttu-id="d59d9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d59d9-112">Description</span></span>                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d59d9-113">CodePage</span><span class="sxs-lookup"><span data-stu-id="d59d9-113">CodePage</span></span> | <span data-ttu-id="d59d9-114">Uma das cadeias de caracteres "932" (japonês), "936" (chinês simplificado), "949" (coreano), "950" (chinês tradicional) ou "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="d59d9-114">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="d59d9-115">Não há suporte para outros valores.</span><span class="sxs-lookup"><span data-stu-id="d59d9-115">No other values are supported.</span></span>                                     |
| <span data-ttu-id="d59d9-116">FromTo</span><span class="sxs-lookup"><span data-stu-id="d59d9-116">FromTo</span></span>   | <span data-ttu-id="d59d9-117">Valor da cadeia de caracteres que consiste em um par de valores hexadecimais de 4 dígitos separados por um hífen (-).</span><span class="sxs-lookup"><span data-stu-id="d59d9-117">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="d59d9-118">Até quatro valores FromTo podem ser especificados, mas cada um deve ser separado do valor anterior por uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="d59d9-118">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="d59d9-119">A seguir estão os valores corretos para a entrada do Registro.</span><span class="sxs-lookup"><span data-stu-id="d59d9-119">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="d59d9-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d59d9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d59d9-121">Entradas do Registro EUDC</span><span class="sxs-lookup"><span data-stu-id="d59d9-121">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="d59d9-122">Eudc</span><span class="sxs-lookup"><span data-stu-id="d59d9-122">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



