---
description: A interface IX509EndorsementKey expõe as propriedades a seguir.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Propriedades de IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749476"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="ca16b-103">Propriedades de IX509EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="ca16b-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="ca16b-104">A interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca16b-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ca16b-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ca16b-105">In this section</span></span>



| <span data-ttu-id="ca16b-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="ca16b-106">Topic</span></span>                                                                        | <span data-ttu-id="ca16b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca16b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca16b-108">**Propriedade Length**</span><span class="sxs-lookup"><span data-stu-id="ca16b-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="ca16b-109">O comprimento de bit da chave de endosso.</span><span class="sxs-lookup"><span data-stu-id="ca16b-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="ca16b-110">Você só pode acessar essa propriedade depois que o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) tiver sido chamado.</span><span class="sxs-lookup"><span data-stu-id="ca16b-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="ca16b-111">**Propriedade aberta**</span><span class="sxs-lookup"><span data-stu-id="ca16b-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="ca16b-112">Indica se o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) foi chamado com êxito.</span><span class="sxs-lookup"><span data-stu-id="ca16b-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="ca16b-113">**Propriedade ProviderName**</span><span class="sxs-lookup"><span data-stu-id="ca16b-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="ca16b-114">O nome do provedor de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ca16b-114">The name of the encryption provider.</span></span> <span data-ttu-id="ca16b-115">O padrão é o provedor Microsoft Platform crypto.</span><span class="sxs-lookup"><span data-stu-id="ca16b-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="ca16b-116">Você deve definir a propriedade [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) antes de chamar o método [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="ca16b-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="ca16b-117">Você não pode alterar a propriedade **ProviderName** depois de ter chamado o método **Open** .</span><span class="sxs-lookup"><span data-stu-id="ca16b-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




