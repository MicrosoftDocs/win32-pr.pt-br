---
description: A função DeviceIoControl fornece uma interface de controle de entrada e saída de dispositivo (IOCTL) por meio da qual um aplicativo pode se comunicar diretamente com um driver de dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Controle de entrada e saída do dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826573"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="884a1-103">Controle de entrada e saída do dispositivo (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="884a1-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="884a1-104">A função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fornece uma interface de controle de entrada e saída de dispositivo (IOCTL) por meio da qual um aplicativo pode se comunicar diretamente com um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="884a1-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="884a1-105">A função **DeviceIoControl** é uma interface de finalidade geral que pode enviar códigos de controle para uma variedade de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="884a1-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="884a1-106">Cada código de controle representa uma operação para o driver executar.</span><span class="sxs-lookup"><span data-stu-id="884a1-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="884a1-107">Por exemplo, um código de controle pode solicitar que um driver de dispositivo retorne informações sobre o dispositivo correspondente ou direcione o driver para executar uma ação no dispositivo, como a formatação de um disco.</span><span class="sxs-lookup"><span data-stu-id="884a1-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="884a1-108">Vários códigos de controle padrão são definidos nos arquivos de cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="884a1-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="884a1-109">Além disso, os drivers de dispositivo podem definir seus próprios códigos de controle específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="884a1-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="884a1-110">Para obter uma lista de códigos de controle padrão incluídos na documentação do SDK, consulte a seção comentários de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="884a1-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="884a1-111">Os tipos de códigos de controle que você pode especificar dependem do dispositivo que está sendo acessado e da plataforma na qual seu aplicativo está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="884a1-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="884a1-112">Os aplicativos podem usar os códigos de controle padrão ou códigos de controle específicos do dispositivo para executar operações de entrada e saída diretas em uma unidade de disquete, unidade de disco rígido, unidade de fita ou unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="884a1-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="884a1-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="884a1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="884a1-114">Chamando DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="884a1-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
