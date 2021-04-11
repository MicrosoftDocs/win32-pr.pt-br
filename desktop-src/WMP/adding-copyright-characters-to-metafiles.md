---
title: Adicionando caracteres de direitos autorais a metaarquivos
description: Os caracteres para os símbolos de registro de direitos autorais e marcas registradas (\ 169; ou \ 174;) podem não ser exibidos corretamente se o metarquivo não for codificado usando o esquema de codificação UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Adicionando caracteres de direitos autorais a metaarquivos do Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293181"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="ad3e9-104">Adicionando caracteres de direitos autorais a metaarquivos</span><span class="sxs-lookup"><span data-stu-id="ad3e9-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="ad3e9-105">Os caracteres de símbolos de registro de direitos autorais e marcas comerciais (© ou®) podem não ser exibidos corretamente se o metarquivo não for codificado usando o esquema de codificação UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="ad3e9-106">Nesse caso, para exibir qualquer um desses símbolos corretamente para todos os usuários, você pode usar os equivalentes ASCII (c) e (r) dentro do elemento de **direitos autorais** , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="ad3e9-107">Se o metarquivo for codificado usando UTF-8, os símbolos de direitos autorais e marcas comerciais serão exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="ad3e9-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad3e9-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad3e9-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3e9-109">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ad3e9-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




