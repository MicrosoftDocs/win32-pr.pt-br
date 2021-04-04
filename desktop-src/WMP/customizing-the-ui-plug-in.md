---
title: Personalizando o plug-in da interface do usuário
description: Personalizando o plug-in da interface do usuário
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-ins do Windows Media Player, personalizando
- plug-ins, personalizando
- plug-ins de interface do usuário, personalizando
- Plug-ins de interface do usuário, personalizando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005927"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="40b82-107">Personalizando o plug-in da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="40b82-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="40b82-108">Neste ponto, seu projeto está pronto para personalização.</span><span class="sxs-lookup"><span data-stu-id="40b82-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="40b82-109">Você pode modificar a implementação gerada pelo assistente da interface **IWMPPluginUI** , pode adicionar uma interface do usuário à classe **CPluginWindow** , e você pode implementar uma página de propriedades na classe **CPropertyDialog** .</span><span class="sxs-lookup"><span data-stu-id="40b82-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="40b82-110">Se o seu plug-in estiver configurado para escutar eventos do Windows Media Player, o assistente terá gerado implementações padrão ou vazias de todos os manipuladores de eventos necessários, que você também modificará ou criará.</span><span class="sxs-lookup"><span data-stu-id="40b82-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="40b82-111">O tipo de plug-in e os recursos aos quais ele dá suporte são indicados por um valor que é armazenado no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="40b82-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="40b82-112">O assistente gera um arquivo com uma extensão de nome de arquivo. rgs que contém as informações para registrar o plug-in com o.</span><span class="sxs-lookup"><span data-stu-id="40b82-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="40b82-113">O valor de "recursos" nesse arquivo é o equivalente Decimal de um booliano ou das constantes de tipo de plug-in e dos sinalizadores de plug-in definidos em wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="40b82-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="40b82-114">Embora esse valor seja determinado pelas opções selecionadas no assistente, você deve modificá-lo se desejar criar um plug-in com várias predefinições ou uma para a qual os itens de mídia ou listas de reprodução possam ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="40b82-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="40b82-115">Conforme você modifica e estende seu código de plug-in, você pode criar e registrar sua DLL para que possa testar seu plug-in no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="40b82-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b82-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40b82-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b82-117">**Criando um plug-in de interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="40b82-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




