---
description: O método SaveBookmark salva a posição e o estado do disco atual do objeto MSWebDVD para que o usuário possa retornar para o mesmo local posteriormente.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766261"
---
# <a name="savebookmark-method"></a><span data-ttu-id="c88ff-103">Método SaveBookmark</span><span class="sxs-lookup"><span data-stu-id="c88ff-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="c88ff-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c88ff-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c88ff-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c88ff-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c88ff-106">O `SaveBookmark` método salva a posição e o estado atuais do disco do objeto **MSWebDVD** para que o usuário possa retornar para o mesmo local posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c88ff-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="c88ff-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c88ff-107">Return Value</span></span>

<span data-ttu-id="c88ff-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c88ff-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88ff-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c88ff-109">Remarks</span></span>

<span data-ttu-id="c88ff-110">Um indicador é um instantâneo do estado atual do navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="c88ff-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="c88ff-111">Isso inclui informações como o local em que ele está sendo reproduzido no disco e quais fluxos de áudio e subimagems são selecionados.</span><span class="sxs-lookup"><span data-stu-id="c88ff-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="c88ff-112">Ao salvar um indicador, o usuário pode fechar o aplicativo, desligar o computador e voltar mais tarde para continuar a exibir o disco certo, onde ele parou, com todas as configurações, assim como estavam antes.</span><span class="sxs-lookup"><span data-stu-id="c88ff-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="c88ff-113">Somente um indicador pode ser salvo em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="c88ff-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="c88ff-114">Quando você chama `SaveBookmark` , o indicador antigo é substituído.</span><span class="sxs-lookup"><span data-stu-id="c88ff-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88ff-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88ff-115">Requirements</span></span>



| <span data-ttu-id="c88ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88ff-116">Requirement</span></span> | <span data-ttu-id="c88ff-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c88ff-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c88ff-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c88ff-118">Header</span></span><br/> | <dl> <span data-ttu-id="c88ff-119"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88ff-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c88ff-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c88ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88ff-121">**RestoreBookmark**</span><span class="sxs-lookup"><span data-stu-id="c88ff-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




