---
title: Configurações do registro de esquema personalizado
description: Configurações do registro de esquema personalizado
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player, configurações de registro de esquema personalizado
- Windows Media Player, esquemas
- Windows Media Player, registro
- registro, configurações de esquema personalizado
- registro, esquemas
- registro, configurações do Windows Media Player
- esquemas
- configurações do registro de esquema personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a02649d9536140fff0ff0d3188a5b25feb49688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005108"
---
# <a name="custom-scheme-registry-settings"></a><span data-ttu-id="fd5f5-111">Configurações do registro de esquema personalizado</span><span class="sxs-lookup"><span data-stu-id="fd5f5-111">Custom Scheme Registry Settings</span></span>

<span data-ttu-id="fd5f5-112">Os esquemas são protocolos personalizados.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-112">Schemes are custom protocols.</span></span> <span data-ttu-id="fd5f5-113">O Windows Media Player mantém uma lista de esquemas no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-113">Windows Media Player maintains a list of schemes in the registry on the user's computer.</span></span> <span data-ttu-id="fd5f5-114">Quando o usuário tenta reproduzir um arquivo de mídia digital, o Player verifica primeiro se o SDK do Windows Media Format dá suporte ao esquema.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-114">When the user attempts to play a digital media file, the Player first checks whether the Windows Media Format SDK supports the scheme.</span></span> <span data-ttu-id="fd5f5-115">Caso contrário, o Player verificará o esquema em relação à lista no registro.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-115">If it doesn't, the Player checks the scheme against the list in the registry.</span></span> <span data-ttu-id="fd5f5-116">Se uma correspondência for encontrada, o Player verificará um valor que indica qual tecnologia subjacente ou *tempo de execução* (como o Microsoft DirectShow ou o Windows Media Format SDK) pode ser usado para reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-116">If a match is found, the Player then checks a value that indicates which underlying technology, or *runtime* (such as Microsoft DirectShow or the Windows Media Format SDK), can be used to play the file.</span></span> <span data-ttu-id="fd5f5-117">Se nenhuma correspondência for encontrada, o Player apresentará ao usuário uma caixa de diálogo de aviso que solicita ao usuário a permissão para tentar reproduzir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-117">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="fd5f5-118">Se você transmitir arquivos de mídia digital usando um esquema de protocolo personalizado, poderá evitar que esse aviso apareça no computador do usuário registrando o esquema e fornecendo um valor para o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-118">If you stream digital media files using a custom protocol scheme, you can prevent this warning from appearing on the user's computer by registering the scheme and providing a value for the runtime.</span></span>

<span data-ttu-id="fd5f5-119">A lista de esquemas é mantida como um conjunto de chaves do registro que correspondem aos esquemas registrados, sem os dois-pontos e as duas barras (://).</span><span class="sxs-lookup"><span data-stu-id="fd5f5-119">The list of schemes is maintained as a set of registry keys that match the registered schemes, without the colon and the two slashes (://).</span></span> <span data-ttu-id="fd5f5-120">Por exemplo, a chave para o esquema wmhtml://, que é usada para transmitir mídia avançada, é denominada "wmhtml".</span><span class="sxs-lookup"><span data-stu-id="fd5f5-120">For example, the key for the wmhtml:// scheme, which is used to stream rich media, is named "wmhtml".</span></span> <span data-ttu-id="fd5f5-121">Uma lista separada é mantida para o computador local e para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-121">A separate list is maintained for the local machine and for each user.</span></span> <span data-ttu-id="fd5f5-122">Para o computador local, as chaves de esquema são subchaves da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="fd5f5-122">For the local machine, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="fd5f5-123">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Schemes\\**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\**</span></span>

<span data-ttu-id="fd5f5-124">Por exemplo, a chave do esquema wmhtml://para o computador local é:</span><span class="sxs-lookup"><span data-stu-id="fd5f5-124">For example, the key for the wmhtml:// scheme for the local machine is:</span></span>

<span data-ttu-id="fd5f5-125">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-125">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="fd5f5-126">Para alterar os valores nessa chave ou criar uma nova subchave, o usuário atual deve ser um administrador do computador.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-126">To change values in this key or to create a new subkey, the current user must be an administrator for the computer.</span></span>

<span data-ttu-id="fd5f5-127">Para usuários individuais, as chaves de esquema são subchaves da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="fd5f5-127">For individual users, the scheme keys are subkeys of the following registry key:</span></span>

<span data-ttu-id="fd5f5-128">**HKEY \_ atual \_ \\ software \\ do usuário \\ esquema do Microsoft MediaPlayer \\ Player \\\\**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\**</span></span>

<span data-ttu-id="fd5f5-129">Por exemplo, a chave para o esquema wmhtml://para o usuário atual é:</span><span class="sxs-lookup"><span data-stu-id="fd5f5-129">For example, the key for the wmhtml:// scheme for the current user is:</span></span>

<span data-ttu-id="fd5f5-130">**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ Schemes \\ wmhtml**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-130">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Schemes\\wmhtml**</span></span>

<span data-ttu-id="fd5f5-131">Ao procurar esquemas registrados, o Player primeiro verifica os valores localizados em **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-131">When checking for registered schemes, the Player first checks the values located in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="fd5f5-132">Se nenhum for encontrado para o esquema atual, o Player em seguida verificará os valores em **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-132">If none are found for the current scheme, the Player next checks the values in **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="fd5f5-133">Se nenhum for encontrado para o esquema atual, o Player exibirá o aviso para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-133">If none are found for the current scheme, the Player displays the warning to the user.</span></span>

<span data-ttu-id="fd5f5-134">Cada subchave de esquema pode conter um dos seguintes valores possíveis para *tempo de execução*.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-134">Each scheme subkey may contain one of the following possible values for *Runtime*.</span></span>



| <span data-ttu-id="fd5f5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fd5f5-135">Value</span></span> | <span data-ttu-id="fd5f5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd5f5-136">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="fd5f5-137">6</span><span class="sxs-lookup"><span data-stu-id="fd5f5-137">6</span></span>     | <span data-ttu-id="fd5f5-138">Renderizar usando o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-138">Render using the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="fd5f5-139">7</span><span class="sxs-lookup"><span data-stu-id="fd5f5-139">7</span></span>     | <span data-ttu-id="fd5f5-140">Renderizar usando o Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-140">Render using Microsoft DirectShow.</span></span>         |



 

<span data-ttu-id="fd5f5-141">Alterar o valor de *tempo de execução* de um esquema que o Windows Media Format SDK suporta não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-141">Changing the *Runtime* value for a scheme that the Windows Media Format SDK supports will have no effect.</span></span> <span data-ttu-id="fd5f5-142">O Player sempre usará o SDK do Windows Media Format como o tempo de execução para esquemas que o Windows Media Format SDK suporta.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-142">The Player will always use the Windows Media Format SDK as the runtime for schemes that the Windows Media Format SDK supports.</span></span> <span data-ttu-id="fd5f5-143">Esse valor de registro foi projetado para permitir a configuração de tempo de execução para esquemas personalizados.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-143">This registry value is designed to allow runtime configuration for custom schemes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd5f5-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd5f5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd5f5-145">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-145">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




