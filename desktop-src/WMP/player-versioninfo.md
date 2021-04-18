---
title: Player. versionInfo
description: A propriedade versionInfo recupera um valor de cadeia de caracteres que especifica a versão do Windows Media Player.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. versionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763330"
---
# <a name="playerversioninfo"></a><span data-ttu-id="8fb6f-104">Player. versionInfo</span><span class="sxs-lookup"><span data-stu-id="8fb6f-104">Player.versionInfo</span></span>

<span data-ttu-id="8fb6f-105">A propriedade **versionInfo** recupera um valor de cadeia de caracteres que especifica a versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb6f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fb6f-106">Syntax</span></span>

<span data-ttu-id="8fb6f-107">*Player* . **versionInfo**</span><span class="sxs-lookup"><span data-stu-id="8fb6f-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="8fb6f-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="8fb6f-108">Possible Values</span></span>

<span data-ttu-id="8fb6f-109">Essa propriedade é uma **cadeia de caracteres** somente leitura no seguinte formato: "*X*. 0,0. *Aaaa*", em que *X* representa o número de versão principal e *yyyy* representa o número de Build.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="8fb6f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8fb6f-110">Examples</span></span>

<span data-ttu-id="8fb6f-111">O exemplo a seguir cria um elemento de botão HTML que, quando clicado, exibe uma caixa de mensagem contendo as informações de versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="8fb6f-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8fb6f-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="8fb6f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fb6f-113">Requirements</span></span>



| <span data-ttu-id="8fb6f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb6f-114">Requirement</span></span> | <span data-ttu-id="8fb6f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8fb6f-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb6f-116">Versão</span><span class="sxs-lookup"><span data-stu-id="8fb6f-116">Version</span></span><br/> | <span data-ttu-id="8fb6f-117">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8fb6f-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8fb6f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb6f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fb6f-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb6f-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb6f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fb6f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb6f-121">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="8fb6f-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





