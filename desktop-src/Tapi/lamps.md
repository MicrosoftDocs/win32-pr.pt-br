---
description: As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lâmpadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011550"
---
# <a name="lamps"></a><span data-ttu-id="b90e2-103">Lâmpadas</span><span class="sxs-lookup"><span data-stu-id="b90e2-103">Lamps</span></span>

<span data-ttu-id="b90e2-104">As lâmpadas em um dispositivo de telefone podem ser acesas em uma variedade de modos de iluminação diferentes.</span><span class="sxs-lookup"><span data-stu-id="b90e2-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="b90e2-105">Ao contrário dos padrões de toque, os modos de lâmpada são mais uniformes em conjuntos de telefone de diferentes fornecedores.</span><span class="sxs-lookup"><span data-stu-id="b90e2-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="b90e2-106">Um conjunto comum de modos de lâmpada é definido pela API.</span><span class="sxs-lookup"><span data-stu-id="b90e2-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="b90e2-107">Uma lâmpada identificada por seu identificador de botão de lâmpada pode ser acesa em um determinado modo de lâmpada.</span><span class="sxs-lookup"><span data-stu-id="b90e2-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="b90e2-108">Uma lâmpada também pode ser consultada para o seu modo de lâmpada atual.</span><span class="sxs-lookup"><span data-stu-id="b90e2-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="b90e2-109">As funções TAPI usadas para lâmpadas são [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), que acende uma lâmpada em um dispositivo de telefone aberto especificado em um determinado modo de iluminação e [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), que retorna o modo de lâmpada atual da lâmpada especificada.</span><span class="sxs-lookup"><span data-stu-id="b90e2-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="b90e2-110">Quando uma lâmpada de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="b90e2-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="b90e2-111">Os parâmetros dessa mensagem fornecem uma indicação da alteração.</span><span class="sxs-lookup"><span data-stu-id="b90e2-111">Parameters to this message provide an indication of the change.</span></span>

 

 



