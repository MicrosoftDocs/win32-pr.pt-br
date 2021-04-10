---
description: A propriedade DVDAdm. BookmarkOnStop define ou recupera um valor que informa ao objeto MSWebDVD se é para salvar automaticamente um indicador do local e das configurações atuais quando o usuário clica no botão parar.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propriedade BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087784"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="4b9eb-103">Propriedade BookmarkOnStop</span><span class="sxs-lookup"><span data-stu-id="4b9eb-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="4b9eb-104">A `DVDAdm.BookmarkOnStop` propriedade define ou recupera um valor que informa ao objeto MSWebDVD se é para salvar automaticamente um indicador do local e das configurações atuais quando o usuário clica no botão **parar** .</span><span class="sxs-lookup"><span data-stu-id="4b9eb-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="4b9eb-105">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4b9eb-105">Return Value</span></span>

<span data-ttu-id="4b9eb-106">Retorna um valor booliano que indica se o objeto MSDVDAdm salvará um indicador de todas as configurações de DVD, incluindo a posição em disco, o nível pai e o país/região pai.</span><span class="sxs-lookup"><span data-stu-id="4b9eb-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b9eb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b9eb-107">Remarks</span></span>

<span data-ttu-id="4b9eb-108">Essa propriedade é de leitura/gravação com um valor padrão de false.</span><span class="sxs-lookup"><span data-stu-id="4b9eb-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="4b9eb-109">Indicadores são válidos somente para um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="4b9eb-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="4b9eb-110">Um usuário não pode salvar um indicador e, em seguida, enviá-lo para outra pessoa para ler em um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="4b9eb-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b9eb-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b9eb-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b9eb-112">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="4b9eb-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="4b9eb-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="4b9eb-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



