---
title: Settings. DefaultFrame
description: A propriedade DefaultFrame especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. DefaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751778"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="ee997-104">Settings. DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="ee997-104">Settings.defaultFrame</span></span>

<span data-ttu-id="ee997-105">A propriedade **DefaultFrame** especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="ee997-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee997-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee997-106">Syntax</span></span>

<span data-ttu-id="ee997-107">Player. Settings. DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="ee997-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="ee997-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="ee997-108">Possible Values</span></span>

<span data-ttu-id="ee997-109">Essa propriedade é uma **cadeia de caracteres** de leitura/gravação correspondente ao valor do atributo **Name** do elemento de quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="ee997-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee997-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee997-110">Remarks</span></span>

<span data-ttu-id="ee997-111">Se um quadro de destino for especificado no próprio evento **ScriptCommand** , essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ee997-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="ee997-112">Essa propriedade é ignorada ao usar o miniaplicativo Java do Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="ee997-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="ee997-113">No navegador, cada comando de script de URL recebido exibe a URL em uma nova janela do navegador, independentemente do valor das *configurações*. **DefaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="ee997-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="ee997-114">**Windows Media Player 10 Mobile**: essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ee997-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee997-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee997-115">Requirements</span></span>



| <span data-ttu-id="ee997-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee997-116">Requirement</span></span> | <span data-ttu-id="ee997-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ee997-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee997-118">Versão</span><span class="sxs-lookup"><span data-stu-id="ee997-118">Version</span></span><br/> | <span data-ttu-id="ee997-119">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ee997-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ee997-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ee997-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ee997-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee997-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee997-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee997-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee997-123">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="ee997-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="ee997-124">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="ee997-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="ee997-125">**Uso do Windows Media Player com o Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="ee997-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





