---
description: Alguns conjuntos de telefone oferecem suporte à noção de baixar dados do ou carregar dados para o dispositivo de telefone, o que permite que o conjunto de telefone seja programado de várias maneiras.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Áreas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781051"
---
# <a name="data-areas"></a><span data-ttu-id="60e56-103">Áreas de dados</span><span class="sxs-lookup"><span data-stu-id="60e56-103">Data Areas</span></span>

<span data-ttu-id="60e56-104">Alguns conjuntos de telefone oferecem suporte à noção de baixar dados do ou carregar dados para o dispositivo de telefone, o que permite que o conjunto de telefone seja programado de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="60e56-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="60e56-105">A TAPI modela esses conjuntos de telefone como tendo uma ou mais áreas de download ou de upload.</span><span class="sxs-lookup"><span data-stu-id="60e56-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="60e56-106">Cada área é identificada por um número que varia de zero para o número de áreas de dados disponíveis no telefone menos uma.</span><span class="sxs-lookup"><span data-stu-id="60e56-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="60e56-107">Os tamanhos de cada área podem variar.</span><span class="sxs-lookup"><span data-stu-id="60e56-107">Sizes of each area can vary.</span></span> <span data-ttu-id="60e56-108">O formato dos dados em si é específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60e56-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="60e56-109">A função TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) baixa um buffer de dados para uma determinada área de dados no dispositivo de telefone, e a função [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) carrega o conteúdo de uma determinada área de dados no dispositivo de telefone para um buffer.</span><span class="sxs-lookup"><span data-stu-id="60e56-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="60e56-110">Quando uma área de dados de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="60e56-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="60e56-111">Os parâmetros dessa mensagem fornecem uma indicação da alteração.</span><span class="sxs-lookup"><span data-stu-id="60e56-111">Parameters to this message provide an indication of the change.</span></span>

 

 



