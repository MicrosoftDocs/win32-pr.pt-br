---
description: A ação RegisterUser registra as informações do usuário com o instalador para identificar o usuário de um produto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Ação RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662143"
---
# <a name="registeruser-action"></a><span data-ttu-id="47024-103">Ação RegisterUser</span><span class="sxs-lookup"><span data-stu-id="47024-103">RegisterUser Action</span></span>

<span data-ttu-id="47024-104">A ação RegisterUser registra as informações do usuário com o instalador para identificar o usuário de um produto.</span><span class="sxs-lookup"><span data-stu-id="47024-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="47024-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="47024-105">Sequence Restrictions</span></span>

<span data-ttu-id="47024-106">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="47024-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="47024-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="47024-107">ActionData Messages</span></span>



| <span data-ttu-id="47024-108">Campo</span><span class="sxs-lookup"><span data-stu-id="47024-108">Field</span></span> | <span data-ttu-id="47024-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="47024-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="47024-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="47024-110">\[1\]</span></span> | <span data-ttu-id="47024-111">Informações de usuário registradas.</span><span class="sxs-lookup"><span data-stu-id="47024-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="47024-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="47024-112">Remarks</span></span>

<span data-ttu-id="47024-113">A ação RegisterUser não é executada durante uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="47024-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="47024-114">Se o identificador do produto inserido pelo usuário não tiver sido validado pela [ação ValidateProductID](validateproductid-action.md), a propriedade [**ProductID**](productid.md) não será definida e essa ação não fará nada.</span><span class="sxs-lookup"><span data-stu-id="47024-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47024-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47024-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47024-116">**USU**</span><span class="sxs-lookup"><span data-stu-id="47024-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="47024-117">**COMPANYNAME**</span><span class="sxs-lookup"><span data-stu-id="47024-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="47024-118">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="47024-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



