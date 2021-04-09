---
description: Quando as estruturas de dados de tamanho variavelmente são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Estruturas de dados de tamanho variavelmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171239"
---
# <a name="variably-sized-data-structures"></a><span data-ttu-id="55d6d-103">Estruturas de dados de tamanho variavelmente</span><span class="sxs-lookup"><span data-stu-id="55d6d-103">Variably Sized Data Structures</span></span>

<span data-ttu-id="55d6d-104">Quando as estruturas de dados de tamanho variavelmente são usadas para transmitir informações entre a TAPI e o aplicativo, o aplicativo é responsável por alocar a memória necessária.</span><span class="sxs-lookup"><span data-stu-id="55d6d-104">When variably sized data structures are used to transmit information between TAPI and the application, the application is responsible for allocating the necessary memory.</span></span> <span data-ttu-id="55d6d-105">A quantidade de memória alocada deve ser pelo menos grande o suficiente para a parte fixa da estrutura de dados e é definida pelo aplicativo no membro **dwTotalSize** da estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="55d6d-105">The amount of memory allocated must be at least large enough for the fixed portion of the data structure, and is set by the application in the **dwTotalSize** member of the data structure.</span></span> <span data-ttu-id="55d6d-106">Os membros **dwUsedSize** e **dwNeededSize** são preenchidos pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="55d6d-106">The **dwUsedSize** and **dwNeededSize** members are filled in by TAPI.</span></span> <span data-ttu-id="55d6d-107">Se **dwTotalSize** for menor que o tamanho da parte fixa, LINEERR/PHONEERR \_ STRUCTURETOOSMALL será retornado.</span><span class="sxs-lookup"><span data-stu-id="55d6d-107">If **dwTotalSize** is less than the size of the fixed portion, then LINEERR/ PHONEERR\_STRUCTURETOOSMALL is returned.</span></span> <span data-ttu-id="55d6d-108">Se uma função retornar êxito, todos os campos na parte fixa terão sido preenchidos.</span><span class="sxs-lookup"><span data-stu-id="55d6d-108">If a function returns success, then all the fields in the fixed portion have been filled in.</span></span> <span data-ttu-id="55d6d-109">Os membros **dwUsedSize** e **dwNeededSize** podem ser comparados para determinar se todas as partes variáveis foram preenchidas e quanto espaço seria necessário para preenchê-las.</span><span class="sxs-lookup"><span data-stu-id="55d6d-109">The **dwUsedSize** and **dwNeededSize** members can be compared to determine if all variable parts have been filled in, and how much space would be required to fill them all in.</span></span>

<span data-ttu-id="55d6d-110">Se **dwNeededSize** for igual a **dwUsedSize**, todas as partes fixas e variáveis serão preenchidas.</span><span class="sxs-lookup"><span data-stu-id="55d6d-110">If **dwNeededSize** is equal to **dwUsedSize**, then all fixed and variable parts have been filled in.</span></span> <span data-ttu-id="55d6d-111">Se **dwNeededSize** for maior que **dwUsedSize**, algumas partes variáveis podem ter sido preenchidas, mas exatamente quais campos de tamanho de variavelmente foram preenchidos são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="55d6d-111">If **dwNeededSize** is larger than **dwUsedSize**, some variable parts may have been filled in, but exactly which variably sized fields have been filled in is undefined.</span></span> <span data-ttu-id="55d6d-112">Nenhuma parte variável é truncada e as partes variáveis que teriam sido truncadas devido a espaço insuficiente são indicadas tendo as partes correspondentes de "deslocamento" e "tamanho" definidas como zero.</span><span class="sxs-lookup"><span data-stu-id="55d6d-112">No variable part is ever truncated, and variable parts that would have been truncated due to insufficient space are indicated by having both of their corresponding "Offset" and "Size" parts set to zero.</span></span> <span data-ttu-id="55d6d-113">Se esses não forem ambos zero (e nenhum erro for retornado), eles indicarão o deslocamento e o tamanho dos dados de parte variável não truncados válidos.</span><span class="sxs-lookup"><span data-stu-id="55d6d-113">If these are not both zero (and no error was returned), they indicate the offset and size of valid, nontruncated variable-part data.</span></span>

<span data-ttu-id="55d6d-114">Um aplicativo sempre pode garantir que todas as partes variáveis sejam preenchidas alocando e indicando **dwNeededSize** bytes para a estrutura e chamando a função "Get" novamente até que a função retorne Success e **dwNeededSize** seja igual a **dwUsedSize**.</span><span class="sxs-lookup"><span data-stu-id="55d6d-114">An application can always guarantee that all variable parts are filled in by allocating and indicating **dwNeededSize** bytes for the structure and calling the "Get" function again until the function returns success and **dwNeededSize** equals **dwUsedSize**.</span></span> <span data-ttu-id="55d6d-115">Isso deve ocorrer na segunda tentativa, exceto pelas condições de corrida que causam alterações no tamanho das partes variáveis entre chamadas, o que deve ser uma ocorrência rara.</span><span class="sxs-lookup"><span data-stu-id="55d6d-115">This should happen on the second try except for race conditions that cause changes in the size of variable parts between calls, which should be a rare occurrence.</span></span>

> [!Note]  
> <span data-ttu-id="55d6d-116">Todas as cadeias de texto, independentemente da codificação, em estruturas de tamanho variadas devem ser terminadas em **nulo** de acordo com as convenções normais de manipulação de cadeia de caracteres C.</span><span class="sxs-lookup"><span data-stu-id="55d6d-116">All text strings, regardless of encoding, in variably sized structures should be **NULL**-terminated according to normal C string-handling conventions.</span></span>

 

 

 



