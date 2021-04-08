---
description: O método Stop interrompe a reprodução.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Método Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922377"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="26d68-103">Método Stop (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="26d68-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="26d68-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="26d68-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="26d68-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="26d68-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="26d68-106">O `Stop` método para a reprodução.</span><span class="sxs-lookup"><span data-stu-id="26d68-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="26d68-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="26d68-107">Return Value</span></span>

<span data-ttu-id="26d68-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="26d68-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d68-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="26d68-109">Remarks</span></span>

<span data-ttu-id="26d68-110">Se [**EnableResetOnStop**](enableresetonstop-property.md) for definido como true, `Stop` a chamada colocará o navegador de DVD, junto com o restante do grafo de filtro, em um estado parado, o que significa que, na próxima vez que o usuário pressionar o botão **reproduzir** , a reprodução será iniciada no início do disco. Se **EnableResetOnStop** for definido como true, a reprodução será retomada de onde parou quando o usuário emitir o comando Next **Play** .</span><span class="sxs-lookup"><span data-stu-id="26d68-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



