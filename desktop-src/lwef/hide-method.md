---
title: Ocultar método
description: Ocultar método
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084506"
---
# <a name="hide-method"></a><span data-ttu-id="295ff-103">Ocultar método</span><span class="sxs-lookup"><span data-stu-id="295ff-103">Hide Method</span></span>

<span data-ttu-id="295ff-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="295ff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="295ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="295ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="295ff-106">Oculta o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="295ff-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="295ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="295ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="295ff-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Ocultar* \*  \[ *rápido*\]</span><span class="sxs-lookup"><span data-stu-id="295ff-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="295ff-109">Parte</span><span class="sxs-lookup"><span data-stu-id="295ff-109">Part</span></span>   | <span data-ttu-id="295ff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="295ff-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="295ff-111">*Rápido*</span><span class="sxs-lookup"><span data-stu-id="295ff-111">*Fast*</span></span> | <span data-ttu-id="295ff-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="295ff-112">Optional.</span></span> <span data-ttu-id="295ff-113">Um valor booliano que indica se a animação associada **ao estado oculto** do caractere deve ser ignorada não reproduz a animação **oculta** .</span><span class="sxs-lookup"><span data-stu-id="295ff-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="295ff-114">**False** (padrão) reproduz a animação de **ocultação** .</span><span class="sxs-lookup"><span data-stu-id="295ff-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="295ff-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="295ff-115">Remarks</span></span>

<span data-ttu-id="295ff-116">O servidor enfileira as ações do método **Hide** na fila do caractere, para que você possa usá-lo para ocultar o caractere após uma sequência de outras animações.</span><span class="sxs-lookup"><span data-stu-id="295ff-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="295ff-117">Você pode executar a ação imediatamente usando o método [**Stop**](stop-method.md) antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="295ff-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="295ff-118">Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="295ff-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="295ff-119">Além disso, se a animação **oculto** associada não tiver sido carregada e você não tiver especificado o parâmetro **Fast** como **true**, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="295ff-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="295ff-120">Portanto, se você estiver usando o protocolo HTTP para acessar dados de caractere ou de animação, use o método [**Get**](get-method.md) e especifique o estado **oculto** para carregar a animação antes de chamar o método **Hide** .</span><span class="sxs-lookup"><span data-stu-id="295ff-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="295ff-121">Ocultar um caractere também pode resultar no disparo do evento [**ActivateInput**](activateinput-event.md) de outro cliente.</span><span class="sxs-lookup"><span data-stu-id="295ff-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="295ff-122">Os caracteres ocultos não podem acessar o canal de áudio.</span><span class="sxs-lookup"><span data-stu-id="295ff-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="295ff-123">O servidor passará um status de falha no evento [**RequestComplete**](requestcomplete-event.md) se você gerar uma solicitação de animação e o caractere estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="295ff-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="295ff-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="295ff-124">See Also</span></span>

[<span data-ttu-id="295ff-125">**Método Show**</span><span class="sxs-lookup"><span data-stu-id="295ff-125">**Show method**</span></span>](show-method.md)


 

