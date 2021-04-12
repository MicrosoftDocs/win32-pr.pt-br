---
title: O método setinfo
description: O método IADs setinfo salva os valores atuais das propriedades para esse Active Directory objeto do cache de propriedades para o repositório de diretório subjacente. Isso é análogo à liberação de um buffer para o disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- ADSI do setinfo, usando
- Propriedades ADSI, salve os valores atuais para propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291776"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="12a1b-106">O método setinfo</span><span class="sxs-lookup"><span data-stu-id="12a1b-106">The SetInfo Method</span></span>

<span data-ttu-id="12a1b-107">O método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) salva os valores atuais das propriedades para esse Active Directory objeto do cache de propriedades para o repositório de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="12a1b-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="12a1b-108">Isso é análogo à liberação de um buffer para o disco.</span><span class="sxs-lookup"><span data-stu-id="12a1b-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="12a1b-109">[**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) atualiza objetos que já existem no diretório ou cria uma nova entrada de diretório para objetos recém-criados.</span><span class="sxs-lookup"><span data-stu-id="12a1b-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="12a1b-110">No momento da chamada [**setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , se algum valor de cache de propriedade tiver sido gravado com um código de controle [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) , como a propriedade ADS \_ \_ Update ou \_ ADS \_ Clear, as solicitações apropriadas serão passadas para o serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="12a1b-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




