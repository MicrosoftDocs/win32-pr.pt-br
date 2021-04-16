---
description: As estruturas de dados usadas pelo TSPI são idênticas àquelas definidas nas estruturas TAPI, com exceção de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Estruturas TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758110"
---
# <a name="tspi-structures"></a><span data-ttu-id="34c89-103">Estruturas TSPI</span><span class="sxs-lookup"><span data-stu-id="34c89-103">TSPI Structures</span></span>

<span data-ttu-id="34c89-104">As estruturas de dados usadas pelo TSPI são idênticas àquelas definidas nas [estruturas TAPI](./tapi-structures.md), com exceção de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span><span class="sxs-lookup"><span data-stu-id="34c89-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="34c89-105">No caso da maioria das estruturas de dados maiores, a responsabilidade pelo preenchimento de membros é dividida entre o provedor de serviços e a TAPI.</span><span class="sxs-lookup"><span data-stu-id="34c89-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="34c89-106">O provedor de serviços deve preservar os valores presentes nos membros de propriedade da TAPI.</span><span class="sxs-lookup"><span data-stu-id="34c89-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="34c89-107">A descrição de quais membros devem ser definidos pelo provedor de serviços e que deve ser preservada é fornecida na seção funções nas funções que se referem a essa estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="34c89-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="34c89-108">Para cada estrutura, a seção de referência lista os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="34c89-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="34c89-109">A finalidade da estrutura</span><span class="sxs-lookup"><span data-stu-id="34c89-109">The purpose of the structure</span></span>
-   <span data-ttu-id="34c89-110">Uma descrição dos valores ou campos</span><span class="sxs-lookup"><span data-stu-id="34c89-110">A description of the values or fields</span></span>
-   <span data-ttu-id="34c89-111">Uma descrição da extensibilidade da estrutura</span><span class="sxs-lookup"><span data-stu-id="34c89-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="34c89-112">Comentários opcionais sobre como usar a estrutura</span><span class="sxs-lookup"><span data-stu-id="34c89-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="34c89-113">Referências opcionais a outras funções, mensagens, constantes ou estruturas.</span><span class="sxs-lookup"><span data-stu-id="34c89-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="34c89-114">Memória para todas as estruturas de dados cuja representação é publicada e compartilhada pela TAPI e o provedor de serviços é alocado pela TAPI ou por um aplicativo que usa a TAPI.</span><span class="sxs-lookup"><span data-stu-id="34c89-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="34c89-115">A TAPI passa um ponteiro para a função TSPI que retorna as informações.</span><span class="sxs-lookup"><span data-stu-id="34c89-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="34c89-116">TSPI preenche a estrutura de dados com as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="34c89-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="34c89-117">Se a operação for assíncrona, as informações não estarão disponíveis até que o retorno de chamada de resposta assíncrona indique êxito.</span><span class="sxs-lookup"><span data-stu-id="34c89-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="34c89-118">Algumas estruturas incluem campos de tamanho e deslocamento para definir o local e o comprimento das cadeias de caracteres na parte variável da estrutura.</span><span class="sxs-lookup"><span data-stu-id="34c89-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="34c89-119">Se o provedor de serviços for solicitado a adicionar uma cadeia de caracteres, mas nenhuma cadeia de caracteres estiver disponível, o provedor de serviços deverá indicar essa condição de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="34c89-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="34c89-120">Defina os campos tamanho e deslocamento como 0.</span><span class="sxs-lookup"><span data-stu-id="34c89-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="34c89-121">Defina o campo de deslocamento para zero, mas o tamanho como 0.</span><span class="sxs-lookup"><span data-stu-id="34c89-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="34c89-122">Defina o campo de deslocamento como diferente de zero, o tamanho como 1 e o byte no deslocamento como 0.</span><span class="sxs-lookup"><span data-stu-id="34c89-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
