---
description: A propriedade CurrentAudioStream define ou recupera o número do fluxo de áudio habilitado.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriedade CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749820"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="5c6b5-103">Propriedade CurrentAudioStream</span><span class="sxs-lookup"><span data-stu-id="5c6b5-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="5c6b5-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5c6b5-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5c6b5-106">A `CurrentAudioStream` propriedade define ou recupera o número do fluxo de áudio habilitado.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="5c6b5-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5c6b5-107">Return Value</span></span>

<span data-ttu-id="5c6b5-108">Retorna um valor inteiro de 0 a 7 indicando o fluxo de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c6b5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c6b5-109">Remarks</span></span>

<span data-ttu-id="5c6b5-110">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-110">This property is read/write with no default value.</span></span> <span data-ttu-id="5c6b5-111">Antes de tentar definir um novo fluxo de áudio, chame [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para verificar se o fluxo está disponível.</span><span class="sxs-lookup"><span data-stu-id="5c6b5-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c6b5-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c6b5-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6b5-113">**AudioStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="5c6b5-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



