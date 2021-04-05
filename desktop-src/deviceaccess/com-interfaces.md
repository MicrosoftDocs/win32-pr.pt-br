---
title: Interfaces COM-acesso ao dispositivo
description: Interfaces de Component Object Model (COM) na API de acesso do dispositivo.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008561"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="9b8b1-103">Interfaces COM-acesso ao dispositivo</span><span class="sxs-lookup"><span data-stu-id="9b8b1-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="9b8b1-104">Interfaces de Component Object Model (COM) na API de acesso do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b8b1-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b8b1-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9b8b1-105">In this section</span></span>

| <span data-ttu-id="9b8b1-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="9b8b1-106">Topic</span></span> | <span data-ttu-id="9b8b1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b8b1-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="9b8b1-108">**ICreateDeviceAccessAsync**</span><span class="sxs-lookup"><span data-stu-id="9b8b1-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="9b8b1-109">A interface [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) é retornada de uma chamada para CreateDeviceAccessInstance.</span><span class="sxs-lookup"><span data-stu-id="9b8b1-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="9b8b1-110">Ele permite que o chamador controle a operação de associação a uma instância de um dispositivo para recuperar outra interface que possa ser usada para interagir com esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b8b1-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="9b8b1-111">**IDeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="9b8b1-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="9b8b1-112">Envia um código de controle para um driver de dispositivo. Essa ação faz com que o dispositivo execute a operação correspondente.</span><span class="sxs-lookup"><span data-stu-id="9b8b1-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="9b8b1-113">**IDeviceRequestCompletionCallback**</span><span class="sxs-lookup"><span data-stu-id="9b8b1-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="9b8b1-114">Fornece um método para lidar com a conclusão de chamadas para o método [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).</span><span class="sxs-lookup"><span data-stu-id="9b8b1-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="9b8b1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b8b1-115">Related topics</span></span>

<span data-ttu-id="9b8b1-116">[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="9b8b1-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
