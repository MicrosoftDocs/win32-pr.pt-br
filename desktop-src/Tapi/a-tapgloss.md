---
description: Os termos a seguir são úteis para entender a tecnologia TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3089d918-78fe-4794-8ba3-3885025cb9c4
title: A (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f264b568c541751eabb1614f1f256ce7789eed84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789879"
---
# <a name="a-telephony-api"></a><span data-ttu-id="1b62f-103">A (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="1b62f-103">A (Telephony API)</span></span>

<span data-ttu-id="1b62f-104">A [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [i](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="1b62f-104">A [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="1b62f-105"><span id="tapi2.analog_display_services_interface_adsi__tapgloss"></span><span id="TAPI2.ANALOG_DISPLAY_SERVICES_INTERFACE_ADSI__TAPGLOSS"></span>**Interface de serviços de vídeo analógico (ADSI)**</span><span class="sxs-lookup"><span data-stu-id="1b62f-105"><span id="tapi2.analog_display_services_interface_adsi__tapgloss"></span><span id="TAPI2.ANALOG_DISPLAY_SERVICES_INTERFACE_ADSI__TAPGLOSS"></span>**Analog Display Services Interface (ADSI)**</span></span>
</dt> <dd>

<span data-ttu-id="1b62f-106">Um padrão Bellcore que define um protocolo no fluxo de informações entre um comutador, um servidor, um sistema de correio de voz ou uma central de serviços, por exemplo, e o telefone, PC, terminal de dados ou outro dispositivo de comunicação com uma tela.</span><span class="sxs-lookup"><span data-stu-id="1b62f-106">A Bellcore standard defining a protocol on the flow of information between a switch, a server, a voice mail system, or service bureau, for example, and a subscriber's telephone, PC, data terminal, or other communicating device with a screen.</span></span> <span data-ttu-id="1b62f-107">A ADSI permite que uma versão de texto da conversa seja exibida na tela durante a conexão telefônica.</span><span class="sxs-lookup"><span data-stu-id="1b62f-107">ADSI enables a text version of the conversation to be displayed on the screen during the telephone connection.</span></span> <span data-ttu-id="1b62f-108">Por exemplo, o usuário disca para uma conta de correio de voz e recebe um menu de áudio para as funções de correio de voz enquanto a tela exibe o menu na forma de texto.</span><span class="sxs-lookup"><span data-stu-id="1b62f-108">As an example, the user dials into a voice mail account and receives an audio menu for the voice mail functions while the screen displays the menu in text form.</span></span>

</dd> <dt>

<span data-ttu-id="1b62f-109"><span id="tapi2.assisted_telephony_tapgloss"></span><span id="TAPI2.ASSISTED_TELEPHONY_TAPGLOSS"></span>**Telefonia assistida**</span><span class="sxs-lookup"><span data-stu-id="1b62f-109"><span id="tapi2.assisted_telephony_tapgloss"></span><span id="TAPI2.ASSISTED_TELEPHONY_TAPGLOSS"></span>**Assisted Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="1b62f-110">O conjunto de funções que não são apenas dedicadas à funcionalidade de telefonia, mas foram projetadas para fazer o estabelecimento de chamadas de voz e chamadas de mídia disponíveis para qualquer aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b62f-110">The set of functions that are not just dedicated to telephonic functionality, but are designed to make the establishment of voice calls and media calls available to any application.</span></span> <span data-ttu-id="1b62f-111">Para obter informações adicionais, consulte [telefonia assistida](./assisted-telephony-overview.md) na visão geral de telefonia.</span><span class="sxs-lookup"><span data-stu-id="1b62f-111">For additional information, see [Assisted Telephony](./assisted-telephony-overview.md) in the telephony overview.</span></span> <span data-ttu-id="1b62f-112">Confira telefonia [*básica*](b-tapgloss.md), [*telefonia estendida*](e-tapgloss.md), [*telefonia suplementar*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="1b62f-112">See [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md), [*Supplementary Telephony*](s-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b62f-113"><span id="tapi2.asynchronous_tapgloss"></span><span id="TAPI2.ASYNCHRONOUS_TAPGLOSS"></span>**manipulador**</span><span class="sxs-lookup"><span data-stu-id="1b62f-113"><span id="tapi2.asynchronous_tapgloss"></span><span id="TAPI2.ASYNCHRONOUS_TAPGLOSS"></span>**asynchronous**</span></span>
</dt> <dd>

<span data-ttu-id="1b62f-114">Método de transmissão de dados que permite que os caracteres sejam enviados em intervalos irregulares em uma linha, precedendo cada caractere com um bit de início e seguindo-o com um bit de parada.</span><span class="sxs-lookup"><span data-stu-id="1b62f-114">Data transmission method that allows characters to be sent at irregular intervals over a line by preceding each character with a start bit and following it with a stop bit.</span></span> <span data-ttu-id="1b62f-115">Consulte [*síncrono*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="1b62f-115">See [*synchronous*](s-tapgloss.md).</span></span>

</dd> </dl>

 

 
