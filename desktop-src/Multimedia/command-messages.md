---
title: Mensagens de comando
description: Mensagens de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensagens de comando MCI, sobre
- Mensagens de comando MCI, sintaxe
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499020"
---
# <a name="command-messages"></a><span data-ttu-id="b81da-106">Mensagens de comando</span><span class="sxs-lookup"><span data-stu-id="b81da-106">Command Messages</span></span>

<span data-ttu-id="b81da-107">A interface de mensagem de comando é projetada para ser usada por aplicativos que exigem uma interface de linguagem C para controlar dispositivos multimídia.</span><span class="sxs-lookup"><span data-stu-id="b81da-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="b81da-108">Ele usa um paradigma de passagem de mensagens para se comunicar com dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="b81da-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="b81da-109">Você pode enviar um comando usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b81da-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="b81da-110">A função **mciSendCommand** retornará zero se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b81da-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="b81da-111">Se a função falhar, a palavra de ordem inferior do valor de retorno conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="b81da-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="b81da-112">Você pode passar esse código de erro para a função [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição de texto do erro.</span><span class="sxs-lookup"><span data-stu-id="b81da-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="b81da-113">Sintaxe das mensagens de comando</span><span class="sxs-lookup"><span data-stu-id="b81da-113">Syntax of Command Messages</span></span>

<span data-ttu-id="b81da-114">As mensagens de comando MCI consistem nos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="b81da-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="b81da-115">Um valor de mensagem constante</span><span class="sxs-lookup"><span data-stu-id="b81da-115">A constant message value</span></span>
-   <span data-ttu-id="b81da-116">Uma estrutura que contém parâmetros para o comando</span><span class="sxs-lookup"><span data-stu-id="b81da-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="b81da-117">Um conjunto de sinalizadores que especificam opções para o comando e validação de campos no bloco de parâmetro</span><span class="sxs-lookup"><span data-stu-id="b81da-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="b81da-118">O exemplo a seguir usa a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar o comando [**MCI \_ Play**](mci-play.md) para o dispositivo identificado por um identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b81da-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="b81da-119">O identificador de dispositivo fornecido no primeiro parâmetro é recuperado quando o dispositivo é aberto usando o comando [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b81da-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="b81da-120">O último parâmetro é o endereço de uma estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) , que pode conter informações sobre onde começar e terminar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="b81da-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="b81da-121">Muitas mensagens de comando MCI usam uma estrutura para conter parâmetros desse tipo.</span><span class="sxs-lookup"><span data-stu-id="b81da-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="b81da-122">O primeiro membro de cada uma dessas estruturas identifica a janela que recebe uma mensagem [**mm \_ MCINOTIFY**](mm-mcinotify.md) quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="b81da-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 