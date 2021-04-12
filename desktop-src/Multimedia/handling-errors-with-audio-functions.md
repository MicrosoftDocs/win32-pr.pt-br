---
title: Tratamento de erros com funções de áudio
description: Tratamento de erros com funções de áudio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- áudio de multimídia, erros de áudio de onda
- áudio, erros de áudio de onda
- áudio de multimídia, erros auxiliares de áudio
- áudio, erros auxiliares de áudio
- áudio de onda, erros
- áudio auxiliar, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293943"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="02f77-109">Tratamento de erros com funções de áudio</span><span class="sxs-lookup"><span data-stu-id="02f77-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="02f77-110">As funções Wave-audio e auxiliar-Audio retornam um valor diferente de zero quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="02f77-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="02f77-111">O Windows fornece funções que convertem esses valores de erro em descrições textuais dos erros.</span><span class="sxs-lookup"><span data-stu-id="02f77-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="02f77-112">O aplicativo ainda deve examinar os valores de erro para determinar como proceder, mas descrições textuais de erros podem ser usadas em caixas de diálogo que descrevem erros para os usuários.</span><span class="sxs-lookup"><span data-stu-id="02f77-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="02f77-113">Você pode usar as seguintes funções para recuperar descrições textuais de valores de erro de áudio:</span><span class="sxs-lookup"><span data-stu-id="02f77-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="02f77-114">Função</span><span class="sxs-lookup"><span data-stu-id="02f77-114">Function</span></span>                                           | <span data-ttu-id="02f77-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="02f77-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="02f77-116">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="02f77-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="02f77-117">Recupera uma descrição textual de um erro de entrada de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="02f77-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="02f77-118">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="02f77-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="02f77-119">Recupera uma descrição textual de um erro de saída de wave-áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="02f77-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="02f77-120">As únicas funções de áudio que não retornam valores de erro são [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)e [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span><span class="sxs-lookup"><span data-stu-id="02f77-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="02f77-121">Essas funções retornarão zero se nenhum dispositivo estiver presente em um sistema ou se encontrar erros.</span><span class="sxs-lookup"><span data-stu-id="02f77-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 