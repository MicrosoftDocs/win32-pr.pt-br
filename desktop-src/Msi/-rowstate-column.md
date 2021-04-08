---
description: O nome da coluna reservada \_ RowState representa o estado não persistente associado a cada linha da tabela em uma tabela de banco de dados do instalador.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010922"
---
# <a name="_rowstate-column"></a><span data-ttu-id="055f8-103">\_Coluna RowState</span><span class="sxs-lookup"><span data-stu-id="055f8-103">\_RowState Column</span></span>

<span data-ttu-id="055f8-104">O nome da coluna reservada \_ RowState representa o estado não persistente associado a cada linha da tabela em uma tabela de banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="055f8-104">The reserved column name \_RowState represents the non-persistent state associated with each table row in an installer database table.</span></span> <span data-ttu-id="055f8-105">A pseudo coluna é do tipo [inteiro](integer.md)e o valor consiste em um conjunto de sinalizadores de bit.</span><span class="sxs-lookup"><span data-stu-id="055f8-105">The pseudo-column is of type [Integer](integer.md), and the value consists of a set of bit flags.</span></span> <span data-ttu-id="055f8-106">Todos os bits são legíveis, mas somente os bits UserInfo e temporários podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="055f8-106">All the bits are readable, but only the UserInfo and Temporary bits can be set.</span></span> <span data-ttu-id="055f8-107">Esses dados só estarão disponíveis se as tabelas estiverem bloqueadas ou em uso (ou seja, enquanto houver uma exibição contendo as tabelas).</span><span class="sxs-lookup"><span data-stu-id="055f8-107">This data is available only as long as the tables are locked or in use (that is, while a view containing the tables exists).</span></span> <span data-ttu-id="055f8-108">A tabela a seguir mostra os atributos que uma linha pode ter.</span><span class="sxs-lookup"><span data-stu-id="055f8-108">The following table shows the attributes a row can have.</span></span>



| <span data-ttu-id="055f8-109">Nome</span><span class="sxs-lookup"><span data-stu-id="055f8-109">Name</span></span>           | <span data-ttu-id="055f8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="055f8-110">Value</span></span> | <span data-ttu-id="055f8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="055f8-111">Meaning</span></span>                                                        |
|----------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="055f8-112">iraUserInfo</span><span class="sxs-lookup"><span data-stu-id="055f8-112">iraUserInfo</span></span>    | <span data-ttu-id="055f8-113">0x01</span><span class="sxs-lookup"><span data-stu-id="055f8-113">0x01</span></span>  | <span data-ttu-id="055f8-114">O atributo é para uso externo.</span><span class="sxs-lookup"><span data-stu-id="055f8-114">The attribute is for external use.</span></span> <span data-ttu-id="055f8-115">Esse valor pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="055f8-115">This value can be updated.</span></span>  |
| <span data-ttu-id="055f8-116">iraTemporary</span><span class="sxs-lookup"><span data-stu-id="055f8-116">iraTemporary</span></span>   | <span data-ttu-id="055f8-117">0x02</span><span class="sxs-lookup"><span data-stu-id="055f8-117">0x02</span></span>  | <span data-ttu-id="055f8-118">A linha não é persistente.</span><span class="sxs-lookup"><span data-stu-id="055f8-118">The row is not persistent.</span></span> <span data-ttu-id="055f8-119">Esse valor pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="055f8-119">This value can be updated.</span></span>          |
| <span data-ttu-id="055f8-120">iraModified</span><span class="sxs-lookup"><span data-stu-id="055f8-120">iraModified</span></span>    | <span data-ttu-id="055f8-121">0x04</span><span class="sxs-lookup"><span data-stu-id="055f8-121">0x04</span></span>  | <span data-ttu-id="055f8-122">Uma linha foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="055f8-122">A row has been updated.</span></span>                                        |
| <span data-ttu-id="055f8-123">iraInserted</span><span class="sxs-lookup"><span data-stu-id="055f8-123">iraInserted</span></span>    | <span data-ttu-id="055f8-124">0x08</span><span class="sxs-lookup"><span data-stu-id="055f8-124">0x08</span></span>  | <span data-ttu-id="055f8-125">Uma linha foi inserida.</span><span class="sxs-lookup"><span data-stu-id="055f8-125">A row has been inserted.</span></span>                                       |
| <span data-ttu-id="055f8-126">iraMergeFailed</span><span class="sxs-lookup"><span data-stu-id="055f8-126">iraMergeFailed</span></span> | <span data-ttu-id="055f8-127">0x0F</span><span class="sxs-lookup"><span data-stu-id="055f8-127">0x0F</span></span>  | <span data-ttu-id="055f8-128">Foi feita uma tentativa de mesclagem com dados não idênticos e não importantes.</span><span class="sxs-lookup"><span data-stu-id="055f8-128">An attempt was made to merge with non-identical, non-key data.</span></span> |



 

<span data-ttu-id="055f8-129">Os bits 6 a 8 são reservados.</span><span class="sxs-lookup"><span data-stu-id="055f8-129">Bits 6 through 8 are reserved.</span></span>

 

 



