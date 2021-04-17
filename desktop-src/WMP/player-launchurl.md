---
title: Método Player. launchURL
description: O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado. | Método Player. launchURL
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- método launchURL Windows Media Player
- método launchURL Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761795"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="1e102-107">Método Player. launchURL</span><span class="sxs-lookup"><span data-stu-id="1e102-107">Player.launchURL method</span></span>

<span data-ttu-id="1e102-108">O método **launchURL** envia uma URL para o navegador padrão do usuário a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="1e102-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e102-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e102-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="1e102-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e102-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e102-111">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1e102-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e102-112">Valor da **cadeia de caracteres** que representa a URL a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="1e102-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e102-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e102-113">Return value</span></span>

<span data-ttu-id="1e102-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1e102-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e102-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e102-115">Remarks</span></span>

<span data-ttu-id="1e102-116">Esse método abre apenas as páginas da Web usando os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1e102-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="1e102-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="1e102-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1e102-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e102-118">Examples</span></span>

<span data-ttu-id="1e102-119">O exemplo a seguir cria um elemento de botão HTML que, quando clicado, exibe o site da Microsoft em uma nova janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="1e102-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="1e102-120">O elemento **Player** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1e102-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="1e102-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e102-121">Requirements</span></span>



| <span data-ttu-id="1e102-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e102-122">Requirement</span></span> | <span data-ttu-id="1e102-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1e102-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e102-124">Versão</span><span class="sxs-lookup"><span data-stu-id="1e102-124">Version</span></span><br/> | <span data-ttu-id="1e102-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1e102-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1e102-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1e102-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e102-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e102-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e102-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e102-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e102-129">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="1e102-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





