---
title: Usando uma função de retorno de chamada para processar mensagens de driver
description: Usando uma função de retorno de chamada para processar mensagens de driver
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- áudio de onda, funções de retorno de chamada
- blocos de dados de áudio, funções de retorno de chamada
- áudio de onda, mensagens de driver de processamento
- blocos de dados de áudio, processando mensagens de driver
- Processando mensagens do driver
- função waveInOpen
- função waveOutOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105787490"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="ac2c6-110">Usando uma função de retorno de chamada para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="ac2c6-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="ac2c6-111">Você pode escrever sua própria função de retorno de chamada para processar mensagens enviadas pelo driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac2c6-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="ac2c6-112">Para usar uma função de retorno de chamada, especifique o sinalizador da função de retorno \_ de chamada no parâmetro *fdwOpen* e o endereço do retorno de chamada no parâmetro *dwCallback* da função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="ac2c6-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="ac2c6-113">As mensagens enviadas a uma função de retorno de chamada são semelhantes às mensagens enviadas a uma janela, exceto que têm dois parâmetros **DWORD** em vez de um parâmetro **uint** e **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ac2c6-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="ac2c6-114">Para obter detalhes sobre essas mensagens, consulte [reproduzindo arquivos de Waveform-Audio](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="ac2c6-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="ac2c6-115">Para passar dados de instância de um aplicativo para uma função de retorno de chamada, use uma das seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="ac2c6-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="ac2c6-116">Passe os dados da instância usando o parâmetro *dwInstance* da função que abre o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac2c6-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="ac2c6-117">Passe os dados da instância usando o membro **dwUser** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica um bloco de dados de áudio que está sendo enviado a um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac2c6-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="ac2c6-118">Se você precisar de mais de 32 bits de dados de instância, passe um ponteiro para uma estrutura que contém as informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="ac2c6-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 