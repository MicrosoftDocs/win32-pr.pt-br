---
description: O monitoramento de dígitos monitora a chamada de dígitos.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Monitoramento de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761969"
---
# <a name="digit-monitoring"></a><span data-ttu-id="c3be3-103">Monitoramento de dígitos</span><span class="sxs-lookup"><span data-stu-id="c3be3-103">Digit Monitoring</span></span>

<span data-ttu-id="c3be3-104">O monitoramento de dígitos monitora a chamada de dígitos.</span><span class="sxs-lookup"><span data-stu-id="c3be3-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="c3be3-105">A TAPI permite que os dígitos sejam sinalizados de acordo com dois métodos (modos de dígitos):</span><span class="sxs-lookup"><span data-stu-id="c3be3-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="c3be3-106">Dígitos de pulso são sinalizados como sequências de pulso ou rotativa.</span><span class="sxs-lookup"><span data-stu-id="c3be3-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="c3be3-107">Para detecção, esses pulsos se manifestam como nada mais do que sequências de cliques audíveis.</span><span class="sxs-lookup"><span data-stu-id="c3be3-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="c3be3-108">Dígitos de pulso válidos são ' 0 ' até ' 9 '.</span><span class="sxs-lookup"><span data-stu-id="c3be3-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="c3be3-109">Os dígitos DTMF são sinalizados como tons de DTMF (frequência dupla de dois tons).</span><span class="sxs-lookup"><span data-stu-id="c3be3-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="c3be3-110">Os dígitos DTMF válidos são ' 0 ' por meio de ' 9 ', ' A '.</span><span class="sxs-lookup"><span data-stu-id="c3be3-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="c3be3-111">' B ', ' C', ' d', ' \* ' e ' \# '.</span><span class="sxs-lookup"><span data-stu-id="c3be3-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="c3be3-112">O início e a borda inferior de dígitos DTMF podem ser monitorados.</span><span class="sxs-lookup"><span data-stu-id="c3be3-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="c3be3-113">Um aplicativo pode habilitar ou desabilitar o monitoramento de dígitos em uma chamada especificada com [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span><span class="sxs-lookup"><span data-stu-id="c3be3-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="c3be3-114">Quando o monitoramento de dígitos está habilitado, os dígitos detectados fazem com que o aplicativo seja notificado com a mensagem de [**linha \_ MONITORDIGITS**](line-monitordigits.md) .</span><span class="sxs-lookup"><span data-stu-id="c3be3-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="c3be3-115">Essa mensagem fornece o identificador de chamada no qual o dígito foi detectado, bem como o valor de dígito e o modo de dígito.</span><span class="sxs-lookup"><span data-stu-id="c3be3-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="c3be3-116">O escopo do monitoramento de dígitos é associado pelo tempo de vida da chamada.</span><span class="sxs-lookup"><span data-stu-id="c3be3-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="c3be3-117">O monitoramento de dígitos em uma chamada termina assim que a chamada *se desconecta* ou fica *ociosa*.</span><span class="sxs-lookup"><span data-stu-id="c3be3-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



