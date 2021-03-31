---
title: Recursos do joystick
description: Recursos do joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrada de multimídia, joysticks
- joysticks, movimento de dois eixos
- joysticks, movimentação de três eixos
- joysticks, botões
- joysticks, intervalos de movimento
- joysticks, frequências de sondagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640954"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="3bcdd-109">Recursos do joystick</span><span class="sxs-lookup"><span data-stu-id="3bcdd-109">Joystick Capabilities</span></span>

<span data-ttu-id="3bcdd-110">Os joysticks podem dar suporte a movimento de dois ou três eixos e até quatro botões.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="3bcdd-111">Os joysticks também dão suporte a diferentes intervalos de *frequências* *de movimento* e pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="3bcdd-112">O intervalo de movimento é a distância que um manipulador de joystick pode mover de sua posição de repouso para a posição mais distante de sua posição de repouso.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="3bcdd-113">A frequência de sondagem é o intervalo de tempo entre as consultas do joystick.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="3bcdd-114">Os drivers de joystick podem dar suporte a um ou dois joysticks.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="3bcdd-115">Você pode determinar o número de joysticks com suporte de um driver de joystick usando a função [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="3bcdd-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="3bcdd-116">Essa função retorna um inteiro sem sinal que contém o número de joysticks com suporte ou zero se não houver suporte a um joystick.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="3bcdd-117">O valor de retorno não indica o número de joysticks anexados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="3bcdd-118">Você pode determinar se um joystick está anexado ao sistema usando a função [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="3bcdd-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="3bcdd-119">Essa função retornará JOYERR \_ NOERROR se o dispositivo especificado estiver anexado.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="3bcdd-120">Caso contrário, retornará JOYERR \_ desconectado.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="3bcdd-121">Cada joystick tem vários recursos que estão disponíveis para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="3bcdd-122">Você pode recuperar os recursos de um joystick usando a função [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="3bcdd-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="3bcdd-123">Essa função preenche uma estrutura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) com recursos de joystick, como os valores mínimo e máximo para seu sistema de coordenadas, o número de botões no joystick e as frequências de sondagem mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="3bcdd-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 