---
description: A função phoneClose fecha o dispositivo de telefone especificado.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Fechando o dispositivo de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502049"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="18b7c-103">Fechando o dispositivo de telefone</span><span class="sxs-lookup"><span data-stu-id="18b7c-103">Closing the Phone Device</span></span>

<span data-ttu-id="18b7c-104">A função [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) fecha o dispositivo de telefone especificado.</span><span class="sxs-lookup"><span data-stu-id="18b7c-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="18b7c-105">O dispositivo de telefone também pode ser fechado à força após o usuário ter modificado a configuração desse telefone ou de seu driver.</span><span class="sxs-lookup"><span data-stu-id="18b7c-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="18b7c-106">Se o usuário quiser que as alterações de configuração sejam efetivas imediatamente (em vez de após a próxima reinicialização do sistema) e afetarem a exibição atual do dispositivo (como uma alteração nos recursos do dispositivo), um provedor de serviços poderá forçar o fechamento do dispositivo telefônico.</span><span class="sxs-lookup"><span data-stu-id="18b7c-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="18b7c-107">Essas mensagens também podem ser enviadas não solicitadas como resultado do dispositivo telefônico que está sendo recuperado de alguma outra maneira.</span><span class="sxs-lookup"><span data-stu-id="18b7c-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="18b7c-108">Portanto, um aplicativo deve estar preparado para lidar com mensagens [**de \_ fechamento de telefone**](phone-close.md) não solicitadas.</span><span class="sxs-lookup"><span data-stu-id="18b7c-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="18b7c-109">No momento em que o dispositivo de telefone é fechado, todas as respostas assíncronas pendentes relacionadas ao dispositivo são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="18b7c-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



