---
description: A chave do registro EUDCCodeRange define intervalos de código EUDC (caracteres definidos pelo usuário final) para várias páginas de código (conjuntos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760360"
---
# <a name="eudccoderange"></a><span data-ttu-id="33fa3-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="33fa3-103">EUDCCodeRange</span></span>

<span data-ttu-id="33fa3-104">A chave do registro EUDCCodeRange define intervalos de código [EUDC (caracteres definidos pelo usuário final)](end-user-defined-characters.md) para várias páginas de código (conjuntos de caracteres).</span><span class="sxs-lookup"><span data-stu-id="33fa3-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="33fa3-105">Ele é usado somente por ferramentas que criam EUDCs e não é de preocupação direta com os usuários do EUDC.</span><span class="sxs-lookup"><span data-stu-id="33fa3-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="33fa3-106">Essa chave do registro tem o seguinte local de registro:</span><span class="sxs-lookup"><span data-stu-id="33fa3-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="33fa3-107">HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="33fa3-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="33fa3-108">O formato é:</span><span class="sxs-lookup"><span data-stu-id="33fa3-108">The format is:</span></span>

<span data-ttu-id="33fa3-109">EUDCCodeRange CodePage = FromTo \[ , deto\]</span><span class="sxs-lookup"><span data-stu-id="33fa3-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="33fa3-110">onde:</span><span class="sxs-lookup"><span data-stu-id="33fa3-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33fa3-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="33fa3-111">CodePage</span></span> | <span data-ttu-id="33fa3-112">Uma das cadeias de caracteres "932" (japonês), "936" (chinês simplificado), "949" (coreano), "950" (chinês tradicional) ou "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="33fa3-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="33fa3-113">Não há suporte para nenhum outro valor.</span><span class="sxs-lookup"><span data-stu-id="33fa3-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="33fa3-114">Deto</span><span class="sxs-lookup"><span data-stu-id="33fa3-114">FromTo</span></span>   | <span data-ttu-id="33fa3-115">Valor da cadeia de caracteres que consiste em um par de valores hexadecimais de 4 dígitos separados por um hífen (-).</span><span class="sxs-lookup"><span data-stu-id="33fa3-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="33fa3-116">Até quatro valores deto podem ser especificados, mas cada um deve ser separado do valor anterior por uma vírgula (,).</span><span class="sxs-lookup"><span data-stu-id="33fa3-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="33fa3-117">A seguir estão os valores corretos para a entrada do registro.</span><span class="sxs-lookup"><span data-stu-id="33fa3-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="33fa3-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33fa3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33fa3-119">Entradas do registro EUDC</span><span class="sxs-lookup"><span data-stu-id="33fa3-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="33fa3-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="33fa3-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



