---
title: Tratamento de erros com funções MIDI
description: Tratamento de erros com funções MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (interface digital de instrumento musical), erros
- MIDI (interface digital de instrumentos musicais), erros
- Serviços MIDI, erros
- Erros de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105748131"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="a2f59-107">Tratamento de erros com funções MIDI</span><span class="sxs-lookup"><span data-stu-id="a2f59-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="a2f59-108">As funções de áudio MIDI retornam um código de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a2f59-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="a2f59-109">Para erros associados a MIDI, as funções [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) e [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperam descrições textuais para os códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="a2f59-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="a2f59-110">O aplicativo ainda deve examinar o valor do erro em si para determinar como proceder, mas pode usar as descrições de erro nas caixas de diálogo para informar os usuários sobre as condições de erro.</span><span class="sxs-lookup"><span data-stu-id="a2f59-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="a2f59-111">As únicas funções de MIDI que não retornam códigos de erro são as funções [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) e [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="a2f59-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="a2f59-112">Essas funções retornarão um valor de zero se nenhum dispositivo estiver presente em um sistema ou se algum erro for encontrado pela função.</span><span class="sxs-lookup"><span data-stu-id="a2f59-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f59-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2f59-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f59-114">Serviços MIDI</span><span class="sxs-lookup"><span data-stu-id="a2f59-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 