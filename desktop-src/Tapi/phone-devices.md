---
description: O suporte a dispositivos telefônicos é suplementar em vez de básico, portanto, os provedores de serviços não precisam dar suporte a dispositivos de telefone.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivos de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921083"
---
# <a name="phone-devices"></a><span data-ttu-id="b1699-103">Dispositivos de telefone</span><span class="sxs-lookup"><span data-stu-id="b1699-103">Phone Devices</span></span>

<span data-ttu-id="b1699-104">O suporte a dispositivos telefônicos é suplementar em vez de básico, portanto, os provedores de serviços não precisam dar suporte a dispositivos de telefone.</span><span class="sxs-lookup"><span data-stu-id="b1699-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="b1699-105">Assim como uma classe de dispositivo de linha é uma abstração de um dispositivo de linha físico, a classe de dispositivo de telefone representa uma abstração independente de dispositivo de um conjunto de telefone.</span><span class="sxs-lookup"><span data-stu-id="b1699-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="b1699-106">A TAPI trata dispositivos de linha e telefone como dispositivos independentes um do outro.</span><span class="sxs-lookup"><span data-stu-id="b1699-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="b1699-107">Em outras palavras, você pode usar um telefone (dispositivo) sem usar uma linha associada, e você pode usar uma linha (dispositivo) sem usar um telefone.</span><span class="sxs-lookup"><span data-stu-id="b1699-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="b1699-108">Provedores de serviços que implementam totalmente essa independência podem oferecer usos para esses dispositivos não definidos por protocolos de telefonia tradicionais.</span><span class="sxs-lookup"><span data-stu-id="b1699-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="b1699-109">Por exemplo, uma pessoa pode usar o fone do telefone da área de trabalho como um dispositivo de áudio de forma de onda para gravação ou reprodução de voz, talvez sem o conhecimento do comutador de que o telefone está em uso.</span><span class="sxs-lookup"><span data-stu-id="b1699-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="b1699-110">Nessa implementação, levantar o fone de telefone local não precisa enviar automaticamente um sinal offhook para o comutador.</span><span class="sxs-lookup"><span data-stu-id="b1699-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="b1699-111">Essa independência também permite que um aplicativo toque o telefone local de maneira independente das chamadas de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1699-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="b1699-112">Os recursos dos provedores de serviços são limitados pelos recursos do hardware e do software usados para interconectar o comutador, o telefone e o computador.</span><span class="sxs-lookup"><span data-stu-id="b1699-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="b1699-113">A TAPI inclui funções para recuperar recursos do dispositivo que permitem aos clientes determinar se esse modelo de uso tem suporte.</span><span class="sxs-lookup"><span data-stu-id="b1699-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="b1699-114">Esta seção descreve os dispositivos de telefone e explica como usar as funções de telefone TAPI para acessar esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b1699-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="b1699-115">Dispositivo de telefone</span><span class="sxs-lookup"><span data-stu-id="b1699-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="b1699-116">Inicialização e desligamento</span><span class="sxs-lookup"><span data-stu-id="b1699-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



