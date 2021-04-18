---
description: A ação ValidateProductID define a propriedade ProductID para o identificador completo do produto.
ms.assetid: 31b2f9d2-98d5-4cf3-af02-f12de2740bb8
title: Ação ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0f9f58641e8e24d73a1acae0b79cc0b875aba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752022"
---
# <a name="validateproductid-action"></a><span data-ttu-id="22c3a-103">Ação ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="22c3a-103">ValidateProductID Action</span></span>

<span data-ttu-id="22c3a-104">A ação ValidateProductID define a propriedade [**ProductID**](productid.md) para o identificador completo do produto.</span><span class="sxs-lookup"><span data-stu-id="22c3a-104">The ValidateProductID action sets the [**ProductID**](productid.md) property to the full product identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="22c3a-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="22c3a-105">Sequence Restrictions</span></span>

<span data-ttu-id="22c3a-106">Essa ação deve ser sequenciada antes do assistente de interface do usuário na [tabela InstallUISequence](installuisequence-table.md) e antes da [ação RegisterUser](registeruser-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="22c3a-106">This action must be sequenced before the user interface wizard in the [InstallUISequence table](installuisequence-table.md) and before the [RegisterUser action](registeruser-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="22c3a-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="22c3a-107">ActionData Messages</span></span>

<span data-ttu-id="22c3a-108">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="22c3a-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c3a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="22c3a-109">Remarks</span></span>

<span data-ttu-id="22c3a-110">O instalador verifica se um produto foi validado com êxito verificando a propriedade [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="22c3a-110">The installer checks whether a product has validated successfully by checking the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="22c3a-111">O instalador define a propriedade **ProductID** para o identificador completo do produto após uma validação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="22c3a-111">The installer sets the **ProductID** property to the full product identifier after a successful validation.</span></span> <span data-ttu-id="22c3a-112">A ação ValidateProductID não fará nada se a propriedade **ProductID** já tiver sido definida por uma validação bem-sucedida ou por outro método.</span><span class="sxs-lookup"><span data-stu-id="22c3a-112">The ValidateProductID action does nothing if the **ProductID** property has already been set by a successful validation or by another method.</span></span>

<span data-ttu-id="22c3a-113">A ação ValidateProductID sempre retorna um sucesso, independentemente de o identificador do produto ser válido, para que o identificador do produto possa ser inserido na linha de comando na primeira vez em que o produto for executado.</span><span class="sxs-lookup"><span data-stu-id="22c3a-113">The ValidateProductID action always returns a success, whether or not the product identifier is valid, so that the product identifier can be entered on the command line the first time the product is run.</span></span>

<span data-ttu-id="22c3a-114">O identificador do produto pode ser validado sem que o usuário insira novamente essas informações definindo a propriedade [**PIDKEY**](pidkey.md) na linha de comando ou usando uma transformação.</span><span class="sxs-lookup"><span data-stu-id="22c3a-114">The product identifier can be validated without having the user reenter this information by setting the [**PIDKEY**](pidkey.md) property on the command line or by using a transform.</span></span> <span data-ttu-id="22c3a-115">A exibição da caixa de diálogo solicitando que o usuário insira o identificador do produto pode então se tornar condicional após a presença da propriedade [**ProductID**](productid.md) , que é definida quando a propriedade **PIDKEY** é validada.</span><span class="sxs-lookup"><span data-stu-id="22c3a-115">The display of the dialog box requesting the user to enter the product identifier can then be made conditional upon the presence of the [**ProductID**](productid.md) property, which is set when the **PIDKEY** property is validated.</span></span>

 

 



