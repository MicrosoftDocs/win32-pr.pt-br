---
title: Gravação de multimídia
description: Gravação de multimídia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Função MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363967"
---
# <a name="multimedia-recording"></a><span data-ttu-id="281f4-105">Gravação de multimídia</span><span class="sxs-lookup"><span data-stu-id="281f4-105">Multimedia Recording</span></span>

<span data-ttu-id="281f4-106">Você pode implementar recursos de gravação em seu aplicativo usando a interface do usuário interna no MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="281f4-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="281f4-107">Você pode usar a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) e a macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para fornecer controles para iniciar e interromper a gravação e salvar as informações gravadas.</span><span class="sxs-lookup"><span data-stu-id="281f4-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="281f4-108">Usando **MCIWndCreate**, você pode especificar estilos de janela para exibir uma janela MCIWnd e incluir o botão **gravar** na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="281f4-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="281f4-109">Usando o **MCIWndNew**, você pode especificar o tipo de dispositivo que está sendo registrado e especificar que as informações serão capturadas em um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="281f4-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="281f4-110">Se seu aplicativo precisar de mais sofisticação, você poderá automatizar e personalizar a gravação usando a macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="281f4-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="281f4-111">Para obter mais informações, consulte [Personalizando o processo de gravação](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="281f4-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="281f4-112">Alguns dispositivos, como CD Audio e MCIAVI, são usados somente para reprodução.</span><span class="sxs-lookup"><span data-stu-id="281f4-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="281f4-113">Outros dispositivos, como, por exemplo, dispositivos de áudio de forma de onda, podem ser usados para gravação.</span><span class="sxs-lookup"><span data-stu-id="281f4-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="281f4-114">Se você especificar um dispositivo que não pode gravar, MCIWnd omitirá o botão **gravar** da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="281f4-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




