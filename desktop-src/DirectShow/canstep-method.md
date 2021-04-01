---
description: O método canstep determina se o decodificador MPEG-2 no sistema local pode executar a revisão do quadro em uma direção especificada.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Método canstep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009917"
---
# <a name="canstep-method"></a><span data-ttu-id="86ce0-103">Método canstep</span><span class="sxs-lookup"><span data-stu-id="86ce0-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="86ce0-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="86ce0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86ce0-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="86ce0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86ce0-106">O `CanStep` método determina se o decodificador MPEG-2 no sistema local pode executar a revisão do quadro em uma direção especificada.</span><span class="sxs-lookup"><span data-stu-id="86ce0-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="86ce0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86ce0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86ce0-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span><span class="sxs-lookup"><span data-stu-id="86ce0-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="86ce0-109">Booliano usado como um sinalizador para especificar a direção, encaminhamento ou retrocesso da capacidade de depuração de quadro do decodificador.</span><span class="sxs-lookup"><span data-stu-id="86ce0-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="86ce0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="86ce0-110">Value</span></span> | <span data-ttu-id="86ce0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="86ce0-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="86ce0-112">true</span><span class="sxs-lookup"><span data-stu-id="86ce0-112">true</span></span>  | <span data-ttu-id="86ce0-113">A etapa do decodificador pode voltar?</span><span class="sxs-lookup"><span data-stu-id="86ce0-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="86ce0-114">false</span><span class="sxs-lookup"><span data-stu-id="86ce0-114">false</span></span> | <span data-ttu-id="86ce0-115">O decodificador pode avançar?</span><span class="sxs-lookup"><span data-stu-id="86ce0-115">Can decoder step forward?</span></span> <span data-ttu-id="86ce0-116">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="86ce0-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86ce0-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="86ce0-117">Return Value</span></span>

<span data-ttu-id="86ce0-118">Retorna um valor booliano de true se o decodificador puder entrar na direção especificada e false caso contrário.</span><span class="sxs-lookup"><span data-stu-id="86ce0-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="86ce0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="86ce0-119">Remarks</span></span>

<span data-ttu-id="86ce0-120">Nem todos os decodificadores de hardware MPEG-2 dão suporte aos novos recursos de revisão de quadros no DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="86ce0-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="86ce0-121">Esse método consulta o decodificador para seus recursos de revisão de quadros.</span><span class="sxs-lookup"><span data-stu-id="86ce0-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="86ce0-122">Se o decodificador puder executar a revisão do quadro, um aplicativo poderá usar o método [**Step**](step-method.md) para percorrer os quadros.</span><span class="sxs-lookup"><span data-stu-id="86ce0-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="86ce0-123">Esse método sempre retornará **true** se um decodificador de software estiver sendo usado.</span><span class="sxs-lookup"><span data-stu-id="86ce0-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



