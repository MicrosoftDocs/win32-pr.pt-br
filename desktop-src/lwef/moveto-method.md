---
title: Método MoveTo
description: Método MoveTo
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007549"
---
# <a name="moveto-method"></a><span data-ttu-id="f4cbc-103">Método MoveTo</span><span class="sxs-lookup"><span data-stu-id="f4cbc-103">MoveTo Method</span></span>

<span data-ttu-id="f4cbc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f4cbc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f4cbc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="f4cbc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbc-106">Move o caractere especificado para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="f4cbc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f4cbc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f4cbc-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  *Velocidade de x, y* \[ \]</span><span class="sxs-lookup"><span data-stu-id="f4cbc-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="f4cbc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f4cbc-109">Part</span></span>    | <span data-ttu-id="f4cbc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4cbc-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cbc-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="f4cbc-111">*x,y*</span></span>   | <span data-ttu-id="f4cbc-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-112">Required.</span></span> <span data-ttu-id="f4cbc-113">Um valor inteiro que indica a borda esquerda (*x*) e a borda superior (*y*) do quadro de animação.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="f4cbc-114">Expresse essas coordenadas em pixels.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="f4cbc-115">*Velocidade*</span><span class="sxs-lookup"><span data-stu-id="f4cbc-115">*Speed*</span></span> | <span data-ttu-id="f4cbc-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-116">Optional.</span></span> <span data-ttu-id="f4cbc-117">Um valor inteiro longo que especifica em milissegundos a velocidade com que o quadro do caractere se move.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="f4cbc-118">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-118">The default value is 1000.</span></span> <span data-ttu-id="f4cbc-119">A especificação de zero (0) move o quadro sem reproduzir uma animação.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4cbc-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4cbc-120">Remarks</span></span>

<span data-ttu-id="f4cbc-121">O servidor desempenha automaticamente a animação apropriada atribuída aos Estados de **movimentação** .</span><span class="sxs-lookup"><span data-stu-id="f4cbc-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="f4cbc-122">O local de um caractere é baseado no canto superior esquerdo de seu quadro.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="f4cbc-123">Se você declarar uma variável de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="f4cbc-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="f4cbc-124">Além disso, se a animação associada não tiver sido carregada no computador local, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="f4cbc-125">Portanto, se você estiver usando o protocolo HTTP para acessar dados de caracteres ou de animação, use o método [**Get**](get-method.md) para carregar as animações de estado de **movimentação** antes de chamar o método **MoveTo** .</span><span class="sxs-lookup"><span data-stu-id="f4cbc-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="f4cbc-126">Mesmo que a animação não seja carregada, o servidor ainda moverá o quadro.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="f4cbc-127">Se você chamar **MoveTo** com um valor diferente de zero antes de o caractere ser mostrado, ele retornará um status de falha se você atribuiu a ele um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) , porque o valor diferente de zero indica que você está tentando reproduzir uma animação quando o caractere não está visível.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="f4cbc-128">O efeito real do parâmetro de *velocidade* pode variar com base na velocidade do processador do computador e na prioridade de outras tarefas em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="f4cbc-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 