---
title: Player. URL
description: A propriedade URL especifica ou recupera o nome do item de mídia a ser reproduzido.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL do Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786144"
---
# <a name="playerurl"></a><span data-ttu-id="db038-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="db038-104">Player.URL</span></span>

<span data-ttu-id="db038-105">A propriedade **URL** especifica ou recupera o nome do item de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="db038-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="db038-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="db038-106">Syntax</span></span>

<span data-ttu-id="db038-107">*Player* . **URL** do</span><span class="sxs-lookup"><span data-stu-id="db038-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="db038-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="db038-108">Possible Values</span></span>

<span data-ttu-id="db038-109">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="db038-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db038-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="db038-110">Remarks</span></span>

<span data-ttu-id="db038-111">Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.</span><span class="sxs-lookup"><span data-stu-id="db038-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="db038-112">Os aplicativos que abrirem itens de mídia atrás de um firewall terão um desempenho melhor se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="db038-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="db038-113">Não chame esse método do código do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="db038-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="db038-114">Solicitando *jogador*. A **URL** de um manipulador de eventos pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="db038-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="db038-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db038-115">Examples</span></span>

<span data-ttu-id="db038-116">O exemplo a seguir cria um elemento de entrada de texto HTML e um elemento de entrada de botão HTML.</span><span class="sxs-lookup"><span data-stu-id="db038-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="db038-117">O elemento TEXT permite que o usuário digite um caminho para especificar um arquivo de mídia digital a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="db038-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="db038-118">O elemento BUTTON executa o JScript que abre o arquivo e inicia o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="db038-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="db038-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="db038-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="db038-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db038-120">Requirements</span></span>



| <span data-ttu-id="db038-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db038-121">Requirement</span></span> | <span data-ttu-id="db038-122">Valor</span><span class="sxs-lookup"><span data-stu-id="db038-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db038-123">Versão</span><span class="sxs-lookup"><span data-stu-id="db038-123">Version</span></span><br/> | <span data-ttu-id="db038-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="db038-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="db038-125">DLL</span><span class="sxs-lookup"><span data-stu-id="db038-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="db038-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db038-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db038-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="db038-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db038-128">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="db038-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





