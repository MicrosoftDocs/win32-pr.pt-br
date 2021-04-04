---
title: Definindo o formato de hora
description: Definindo o formato de hora
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823714"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="f8444-104">Definindo o formato de hora</span><span class="sxs-lookup"><span data-stu-id="f8444-104">Setting the Time Format</span></span>

<span data-ttu-id="f8444-105">Use a mensagem de comando [**\_ set do MCI**](mci-set.md) junto com a estrutura do [**MCI \_ set \_ parms**](mci-set-parms.md) para definir o formato de hora para um dispositivo aberto.</span><span class="sxs-lookup"><span data-stu-id="f8444-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="f8444-106">Defina o membro **dwTimeFormat** como uma das constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8444-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="f8444-107">Constante</span><span class="sxs-lookup"><span data-stu-id="f8444-107">Constant</span></span>                   | <span data-ttu-id="f8444-108">Formato de hora</span><span class="sxs-lookup"><span data-stu-id="f8444-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="f8444-109">\_bytes de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f8444-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="f8444-110">Bytes (em arquivos de formato PCM modulados por código de pulso \[ \] )</span><span class="sxs-lookup"><span data-stu-id="f8444-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="f8444-111">\_milissegundos do formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f8444-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="f8444-112">Milissegundos</span><span class="sxs-lookup"><span data-stu-id="f8444-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="f8444-113">\_formato MCI \_ MSF</span><span class="sxs-lookup"><span data-stu-id="f8444-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="f8444-114">Minuto/segundo/quadro</span><span class="sxs-lookup"><span data-stu-id="f8444-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="f8444-115">\_exemplos de formato MCI \_</span><span class="sxs-lookup"><span data-stu-id="f8444-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="f8444-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8444-116">Samples</span></span>                                              |
| <span data-ttu-id="f8444-117">\_Formato MCI \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="f8444-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="f8444-118">SMPTE, 24 frame</span><span class="sxs-lookup"><span data-stu-id="f8444-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="f8444-119">\_Formato MCI \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="f8444-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="f8444-120">SMPTE, 25 quadros</span><span class="sxs-lookup"><span data-stu-id="f8444-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="f8444-121">\_Formato MCI \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="f8444-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="f8444-122">SMPTE, 30 quadros</span><span class="sxs-lookup"><span data-stu-id="f8444-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="f8444-123">\_Formato MCI \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="f8444-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="f8444-124">SMPTE, 30 quadros drop</span><span class="sxs-lookup"><span data-stu-id="f8444-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="f8444-125">\_formato MCI \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="f8444-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="f8444-126">Faixa/minuto/segundo/quadro</span><span class="sxs-lookup"><span data-stu-id="f8444-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="f8444-127">\_formato de Seq MCI \_ \_ SONGPTR</span><span class="sxs-lookup"><span data-stu-id="f8444-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="f8444-128">Ponteiro de música MIDI</span><span class="sxs-lookup"><span data-stu-id="f8444-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="f8444-129">O exemplo a seguir define o formato de hora como milissegundos no dispositivo especificado pela variável wDeviceID usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f8444-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 