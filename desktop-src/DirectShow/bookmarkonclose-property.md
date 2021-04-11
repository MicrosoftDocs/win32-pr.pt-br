---
description: A propriedade DVDAdm. BookmarkOnClose define ou recupera um valor que informa ao objeto MSDVDAdm se deve salvar automaticamente um indicador do local atual e as configurações quando o usuário fechar o aplicativo.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propriedade BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296034"
---
# <a name="bookmarkonclose-property"></a><span data-ttu-id="91d14-103">Propriedade BookmarkOnClose</span><span class="sxs-lookup"><span data-stu-id="91d14-103">BookmarkOnClose Property</span></span>

> [!Note]  
> <span data-ttu-id="91d14-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91d14-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="91d14-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="91d14-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="91d14-106">A `DVDAdm.BookmarkOnClose` propriedade define ou recupera um valor que informa ao objeto MSDVDAdm se deve salvar automaticamente um indicador do local atual e as configurações quando o usuário fechar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="91d14-106">The `DVDAdm.BookmarkOnClose` property sets or retrieves a value that tells the MSDVDAdm object whether to automatically save a bookmark of the current location and settings when the user closes the application.</span></span>

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a><span data-ttu-id="91d14-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="91d14-107">Return Value</span></span>

<span data-ttu-id="91d14-108">Retorna um valor booliano, que, se true, indica que o controle MSDVDAdm salvará um indicador de todas as configurações de DVD, incluindo a posição em disco, o nível pai e o país/região pai quando o usuário fechar o aplicativo de DVD Player.</span><span class="sxs-lookup"><span data-stu-id="91d14-108">Returns a Boolean value, which if true, indicates that the MSDVDAdm control will save a bookmark of all DVD settings, including position on disc, parental level, and parental country/region when the user closes the DVD player application.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d14-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="91d14-109">Remarks</span></span>

<span data-ttu-id="91d14-110">Essa propriedade é de leitura/gravação com um valor padrão de true.</span><span class="sxs-lookup"><span data-stu-id="91d14-110">This property is read/write with a default value of true.</span></span>

## <a name="see-also"></a><span data-ttu-id="91d14-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="91d14-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d14-112">**BookmarkOnStop**</span><span class="sxs-lookup"><span data-stu-id="91d14-112">**BookmarkOnStop**</span></span>](bookmarkonstop-property.md)
</dt> <dt>

[<span data-ttu-id="91d14-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="91d14-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



