---
description: O método StillOff retoma a reprodução, cancelando o modo ainda.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Método StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780040"
---
# <a name="stilloff-method"></a><span data-ttu-id="5c8ef-103">Método StillOff</span><span class="sxs-lookup"><span data-stu-id="5c8ef-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="5c8ef-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5c8ef-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5c8ef-106">O `StillOff` método retoma a reprodução, cancelando o modo ainda.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="5c8ef-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5c8ef-107">Return Value</span></span>

<span data-ttu-id="5c8ef-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8ef-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c8ef-109">Remarks</span></span>

<span data-ttu-id="5c8ef-110">O [navegador de DVD](dvd-navigator-filter.md) entra em modo ainda quando encontra um quadro ainda criado no disco. Ele notifica seu aplicativo enviando um \_ evento do EC DVD \_ ainda \_ .</span><span class="sxs-lookup"><span data-stu-id="5c8ef-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="5c8ef-111">O modo ainda é diferente do DVD Navigator estar em um estado pausado devido a uma operação de usuário.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="5c8ef-112">Chamar `StillOff` retoma a reprodução a partir do modo ainda, mas não reinicia o navegador de DVD quando ele está em um estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="5c8ef-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



