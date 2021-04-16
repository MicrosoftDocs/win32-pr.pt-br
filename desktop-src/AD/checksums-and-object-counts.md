---
title: Somas de verificação e contagens de objetos
description: Somas de verificação e contagens de objetos são estratégias de detecção que permitem que um aplicativo detecte um estado de atualização parcial.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453474"
---
# <a name="checksums-and-object-counts"></a><span data-ttu-id="7c785-103">Somas de verificação e contagens de objetos</span><span class="sxs-lookup"><span data-stu-id="7c785-103">Checksums and Object Counts</span></span>

<span data-ttu-id="7c785-104">Somas de verificação e contagens de objetos são estratégias de detecção que permitem que um aplicativo detecte um estado de atualização parcial.</span><span class="sxs-lookup"><span data-stu-id="7c785-104">Checksums and object counts are detection strategies that allow an application to detect a partial update state.</span></span> <span data-ttu-id="7c785-105">As somas de verificação também podem ser usadas para detectar inconsistências introduzidas pela resolução de colisão.</span><span class="sxs-lookup"><span data-stu-id="7c785-105">Checksums can also be used to detect inconsistencies introduced by collision resolution.</span></span> <span data-ttu-id="7c785-106">As somas de verificação e as contagens de objeto exigem um local para armazenar o valor usado para verificar uma soma de verificação ou contagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="7c785-106">Both checksums and object counts require a place to store the value used for verifying a checksum or object count.</span></span> <span data-ttu-id="7c785-107">Isso pode ser um objeto "mestre" escolhido entre os envolvidos na relação específica do aplicativo ou em um objeto pai sob o qual os objetos relacionados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="7c785-107">This can be on a "master" object chosen from among those involved in the application-specific relationship or on a parent object under which the related objects are stored.</span></span>

<span data-ttu-id="7c785-108">Para somas de verificação, os aplicativos que lêem os objetos relacionados verificam a soma de verificação calculando um resultado local e comparando-o com o valor armazenado.</span><span class="sxs-lookup"><span data-stu-id="7c785-108">For checksums, applications reading the related objects verify the checksum by calculating a local result and comparing it with the stored value.</span></span> <span data-ttu-id="7c785-109">Se os valores não corresponderem, a réplica estará em um estado de atualização parcial e os objetos não poderão ser usados.</span><span class="sxs-lookup"><span data-stu-id="7c785-109">If the values do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="7c785-110">Para contagens de objetos, os aplicativos contam os objetos relacionados (normalmente filhos de um único pai) e comparam a contagem com o valor armazenado.</span><span class="sxs-lookup"><span data-stu-id="7c785-110">For object counts, applications count the related objects (typically children of a single parent) and compare the count with the stored value.</span></span> <span data-ttu-id="7c785-111">Se as contagens não corresponderem, a réplica estará em um estado de atualização parcial e os objetos não poderão ser usados.</span><span class="sxs-lookup"><span data-stu-id="7c785-111">If the counts do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="7c785-112">Algumas considerações importantes:</span><span class="sxs-lookup"><span data-stu-id="7c785-112">Some important considerations:</span></span>

-   <span data-ttu-id="7c785-113">Para que a abordagem de soma de verificação funcione, é necessário atualizar um ou mais atributos usados na computação da soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="7c785-113">For the checksum approach to work, the one or more attributes used in computing the checksum must be updated.</span></span> <span data-ttu-id="7c785-114">O algoritmo usado para calcular a soma de verificação deve refletir as diferenças na entrada de forma confiável.</span><span class="sxs-lookup"><span data-stu-id="7c785-114">The algorithm used to compute the checksum must reliably reflect differences in input.</span></span> <span data-ttu-id="7c785-115">Se muitas entradas diferentes contiverem a mesma soma de verificação, o algoritmo não detectará as atualizações parciais de forma confiável.</span><span class="sxs-lookup"><span data-stu-id="7c785-115">If many different inputs product the same checksum, the algorithm will not reliably detect partial updates.</span></span> <span data-ttu-id="7c785-116">"Salting" a entrada com valores como o **objectGUID** do computador de origem e a data e hora da atualização também é útil.</span><span class="sxs-lookup"><span data-stu-id="7c785-116">"Salting" the input with values like the **objectGUID** of the source computer and the date and time of the update is also helpful.</span></span>
-   <span data-ttu-id="7c785-117">As contagens de objetos funcionam melhor quando usadas com novos conjuntos de objetos ou em combinação com GUIDs de consistência (consulte a próxima seção para obter mais informações).</span><span class="sxs-lookup"><span data-stu-id="7c785-117">Object counts work best when used with new sets of objects, or in combination with consistency GUIDs (see the next section for more information).</span></span> <span data-ttu-id="7c785-118">O aplicativo que está executando a atualização deve saber, antecipadamente, o número de objetos que estarão no contêiner quando a atualização for concluída ou use outros meios de marcar o contêiner como inválido enquanto a atualização continuar (por exemplo, definindo a contagem como zero).</span><span class="sxs-lookup"><span data-stu-id="7c785-118">The application performing the update must either know, in advance, the number of objects that will be in the container when the update is completed or use some other means of marking the container invalid while the update proceeds (for example, setting the count to zero).</span></span> <span data-ttu-id="7c785-119">Depois de concluir a atualização, o aplicativo de origem marca o contêiner com a contagem de objetos contidos.</span><span class="sxs-lookup"><span data-stu-id="7c785-119">After completing the update the source application marks the container with the count of objects contained.</span></span>

 

 




