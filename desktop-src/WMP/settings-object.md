---
title: Objeto de configurações (SDK do Windows Media Player)
description: O objeto Settings fornece uma maneira de modificar várias configurações do Windows Media Player usando as propriedades e os métodos a seguir.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objeto de configurações Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103823431"
---
# <a name="settings-object"></a><span data-ttu-id="ceb79-104">Objeto de configurações</span><span class="sxs-lookup"><span data-stu-id="ceb79-104">Settings Object</span></span>

<span data-ttu-id="ceb79-105">O objeto **Settings** fornece uma maneira de modificar várias configurações do Windows Media Player usando as propriedades e os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceb79-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="ceb79-106">O objeto de **configurações** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceb79-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="ceb79-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ceb79-107">Property</span></span>                                                  | <span data-ttu-id="ceb79-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ceb79-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb79-109">Inicialização automática</span><span class="sxs-lookup"><span data-stu-id="ceb79-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="ceb79-110">Especifica ou recupera um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ceb79-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="ceb79-111">Lance</span><span class="sxs-lookup"><span data-stu-id="ceb79-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="ceb79-112">Especifica ou recupera o saldo de estéreo atual.</span><span class="sxs-lookup"><span data-stu-id="ceb79-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="ceb79-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="ceb79-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="ceb79-114">Especifica ou recupera a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos em arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="ceb79-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="ceb79-115">defaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="ceb79-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="ceb79-116">Recupera o LCID (identificador de localidade) do idioma de áudio padrão especificado no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ceb79-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="ceb79-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="ceb79-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="ceb79-118">Especifica ou recupera o nome do quadro usado para exibir uma URL recebida em um evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="ceb79-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="ceb79-119">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="ceb79-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="ceb79-120">Especifica ou recupera um valor que indica se as caixas de diálogo de erro são mostradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ceb79-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="ceb79-121">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="ceb79-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="ceb79-122">Especifica ou recupera um valor que indica se os eventos de URL devem iniciar um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="ceb79-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="ceb79-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="ceb79-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="ceb79-124">Recupera se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="ceb79-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="ceb79-125">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="ceb79-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="ceb79-126">Recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ceb79-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="ceb79-127">Muta</span><span class="sxs-lookup"><span data-stu-id="ceb79-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="ceb79-128">Especifica ou recupera um valor que indica se o áudio está mudo.</span><span class="sxs-lookup"><span data-stu-id="ceb79-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="ceb79-129">playCount</span><span class="sxs-lookup"><span data-stu-id="ceb79-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="ceb79-130">Especifica ou recupera o número de vezes que um item de mídia será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="ceb79-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="ceb79-131">frequência</span><span class="sxs-lookup"><span data-stu-id="ceb79-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="ceb79-132">Especifica ou recupera a taxa de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="ceb79-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="ceb79-133">volume</span><span class="sxs-lookup"><span data-stu-id="ceb79-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="ceb79-134">Especifica ou recupera o volume atual.</span><span class="sxs-lookup"><span data-stu-id="ceb79-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="ceb79-135">O objeto de **configurações** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceb79-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="ceb79-136">Método</span><span class="sxs-lookup"><span data-stu-id="ceb79-136">Method</span></span>                                                            | <span data-ttu-id="ceb79-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="ceb79-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="ceb79-138">GetMode</span><span class="sxs-lookup"><span data-stu-id="ceb79-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="ceb79-139">Determina se o modo de loop ou de ordem aleatória está ativo.</span><span class="sxs-lookup"><span data-stu-id="ceb79-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="ceb79-140">requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="ceb79-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="ceb79-141">Solicita um nível especificado de acesso à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ceb79-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="ceb79-142">setmode</span><span class="sxs-lookup"><span data-stu-id="ceb79-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="ceb79-143">Define o modo de loop ou de ordem aleatória como ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="ceb79-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="ceb79-144">O objeto **Settings** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceb79-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="ceb79-145">Objeto</span><span class="sxs-lookup"><span data-stu-id="ceb79-145">Object</span></span>                      | <span data-ttu-id="ceb79-146">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ceb79-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="ceb79-147">Jogador</span><span class="sxs-lookup"><span data-stu-id="ceb79-147">Player</span></span>](player-object.md) | [<span data-ttu-id="ceb79-148">configurações</span><span class="sxs-lookup"><span data-stu-id="ceb79-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="ceb79-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceb79-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb79-150">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="ceb79-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




