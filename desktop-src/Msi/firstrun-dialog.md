---
description: Uma sequência da caixa de diálogo FirstRun coleta o nome do usuário, o nome da empresa e as informações de ID do produto. O instalador verifica a ID do produto durante esta caixa de diálogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Caixa de diálogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165001"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="1dda6-104">Caixa de diálogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="1dda6-104">FirstRun Dialog</span></span>

<span data-ttu-id="1dda6-105">Uma sequência da caixa de diálogo FirstRun coleta o nome do usuário, o nome da empresa e as informações de ID do produto.</span><span class="sxs-lookup"><span data-stu-id="1dda6-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="1dda6-106">O instalador verifica a ID do produto durante esta caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1dda6-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="1dda6-107">Uma sequência de caixa de diálogo FirstRun geralmente não faz parte da sequência de ação e é chamada pela função [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) na primeira execução do produto.</span><span class="sxs-lookup"><span data-stu-id="1dda6-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="1dda6-108">Um autor de um pacote do instalador pode usar a sequência de diálogo de modelo ou criar uma sequência diferente.</span><span class="sxs-lookup"><span data-stu-id="1dda6-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="1dda6-109">No entanto, a sequência de diálogo precisa ter o usuário definido as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="1dda6-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="1dda6-110">Propriedade [**username**](username.md)</span><span class="sxs-lookup"><span data-stu-id="1dda6-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="1dda6-111">Propriedade [**CompanyName**](companyname.md)</span><span class="sxs-lookup"><span data-stu-id="1dda6-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="1dda6-112">Propriedade [**PIDKEY**](pidkey.md)</span><span class="sxs-lookup"><span data-stu-id="1dda6-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="1dda6-113">A ID do produto será validada durante a caixa de diálogo usando a [ação ValidateProductID](validateproductid-action.md) ou [ValidateProductID ControlEvent,](validateproductid-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="1dda6-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="1dda6-114">Se a ID do produto for definida como uma propriedade na linha de comando ou por uma transformação, a necessidade de fazer com que o usuário insira novamente a ID do produto durante a caixa de diálogo de primeira execução poderá ser contornada controlando a exibição usando a propriedade [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="1dda6-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="1dda6-115">Após a validação bem-sucedida da ID do produto, a propriedade **ProductID** é definida como a ID de produto completa válida.</span><span class="sxs-lookup"><span data-stu-id="1dda6-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



