---
title: Plataforma de sensor
description: O Windows 7 mudou como os desenvolvedores usam sensores.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007785"
---
# <a name="sensor-platform"></a><span data-ttu-id="089fe-103">Plataforma de sensor</span><span class="sxs-lookup"><span data-stu-id="089fe-103">Sensor Platform</span></span>

<span data-ttu-id="089fe-104">O Windows 7 mudou como os desenvolvedores usam sensores.</span><span class="sxs-lookup"><span data-stu-id="089fe-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="089fe-105">Ele inclui suporte nativo para sensores, expandido por uma nova plataforma de desenvolvimento para trabalhar com sensores, incluindo sensores de localização, como dispositivos GPS (Global Positioning Systems).</span><span class="sxs-lookup"><span data-stu-id="089fe-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="089fe-106">Criado na plataforma do sensor, as APIs de *localização do Windows* são um novo recurso do Windows 7 que permite que os desenvolvedores de aplicativos acessem as informações de local físico do usuário.</span><span class="sxs-lookup"><span data-stu-id="089fe-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="089fe-107">As APIs de *localização do Windows* podem abstrair hardware, dar suporte simultâneo a vários aplicativos e alternar diretamente entre diferentes tecnologias, aliviando o desenvolvedor do aplicativo da carga de gerenciar essas restrições.</span><span class="sxs-lookup"><span data-stu-id="089fe-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="089fe-108">As APIs de *localização* podem ser usadas pelos programadores por meio da linguagem de programação C++ (por programadores familiarizados com Component Object Model (com)) ou usando objetos com em linguagens de script, como o Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="089fe-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="089fe-109">O suporte a scripts fornece fácil acesso a dados de localização para projetos como gadgets.</span><span class="sxs-lookup"><span data-stu-id="089fe-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="089fe-110">O Windows 7 fornece uma plataforma sólida e fácil de usar para usar dispositivos de sensor, como um sensor de luz ambiente ou um medidor de temperatura, para criar conscientização ambiental em aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="089fe-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="089fe-111">Os computadores podem usar sensores que são incorporados ao computador, conectados por meio de conexões com ou sem fio, ou conectados por meio de uma rede ou da *Internet*.</span><span class="sxs-lookup"><span data-stu-id="089fe-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="089fe-112">As APIs do *sensor* e do *local* fornecem uma maneira padrão de descobrir sensores e acessar programaticamente os dados que os sensores fornecem.</span><span class="sxs-lookup"><span data-stu-id="089fe-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="089fe-113">O painel de controle do *sensor* permite que os usuários habilitem ou desabilitem sensores, controlem o acesso a sensores que podem expor dados confidenciais, exibir propriedades do sensor e alterar as descrições dos sensores.</span><span class="sxs-lookup"><span data-stu-id="089fe-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="089fe-114">A [extensão de classe de sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) é uma parte principal do modelo de desenvolvimento de driver para a plataforma do sensor.</span><span class="sxs-lookup"><span data-stu-id="089fe-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="089fe-115">Ele fornece os seguintes mecanismos, que são usados ao escrever um driver de sensor de [estrutura de driver de modo de usuário (UMDF)](https://developer.microsoft.com/windows/hardware) :</span><span class="sxs-lookup"><span data-stu-id="089fe-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="089fe-116">Integração com a plataforma do sensor</span><span class="sxs-lookup"><span data-stu-id="089fe-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="089fe-117">Imposição de segurança</span><span class="sxs-lookup"><span data-stu-id="089fe-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="089fe-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="089fe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="089fe-119">API de sensor</span><span class="sxs-lookup"><span data-stu-id="089fe-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>