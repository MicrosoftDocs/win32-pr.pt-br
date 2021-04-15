---
title: Consultando informações de direitos simples
description: Consultando informações de direitos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- SDK do Windows Media Format, consultando direitos simples
- SDK do Windows Media Format, consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultando direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- DRM (gerenciamento de direitos digitais), consultas de direitos simples
- APIs estendidas do cliente DRM, consultando direitos simples
- APIs estendidas do cliente, consultando direitos simples
- APIs estendidas do cliente DRM, consultas de direitos simples
- APIs estendidas do cliente, consultas de direitos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364014"
---
# <a name="querying-for-simple-rights-information"></a><span data-ttu-id="650ce-113">Consultando informações de direitos simples</span><span class="sxs-lookup"><span data-stu-id="650ce-113">Querying for Simple Rights Information</span></span>

<span data-ttu-id="650ce-114">As APIs estendidas do cliente DRM do Windows Media permitem que você obtenha rapidamente informações simples sobre se o conteúdo protegido pode ser acessado para várias ações.</span><span class="sxs-lookup"><span data-stu-id="650ce-114">The Windows Media DRM Client Extended APIs enable you to quickly get simple information about whether protected content can be accessed for various actions.</span></span>

<span data-ttu-id="650ce-115">O método [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) pode ser usado para determinar rapidamente se uma ação é permitida por uma licença no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="650ce-115">The [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method can be used to determine quickly whether an action is permitted by a license in the local license store.</span></span> <span data-ttu-id="650ce-116">O **QueryActionAllowed** foi otimizado para ser muito mais rápido do que as consultas de informações semelhantes usando os objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="650ce-116">**QueryActionAllowed** has been optimized to be much faster than queries for similar information using the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="650ce-117">No entanto, esse tipo de consulta agrega as licenças no repositório de licenças local e deve ser usado somente para recursos simples, como pode ser necessário para elementos da interface do usuário, por exemplo, exibindo um indicador de permissão.</span><span class="sxs-lookup"><span data-stu-id="650ce-117">However, this type of query aggregates the licenses in the local license store and should be used only for simple features, such as might be needed for user interface elements, for example displaying a permission indicator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="650ce-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="650ce-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="650ce-119">**Obtendo informações de licenças no repositório de licenças local**</span><span class="sxs-lookup"><span data-stu-id="650ce-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




