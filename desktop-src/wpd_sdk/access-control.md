---
description: Controle de acesso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Controle de acesso (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837016"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="5e5a0-103">Controle de acesso (API WPD)</span><span class="sxs-lookup"><span data-stu-id="5e5a0-103">Access Control (WPD API)</span></span>

<span data-ttu-id="5e5a0-104">O Windows Driver Model (WDM) dá suporte à restrição de acesso a dispositivos por meio de ACLs (listas de controle de acesso) nos nós de dispositivo de Plug and Play (PnP).</span><span class="sxs-lookup"><span data-stu-id="5e5a0-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="5e5a0-105">Isso significa que os fornecedores e os administradores de rede podem restringir o acesso a qualquer tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="5e5a0-106">Quando um aplicativo abre um identificador para um driver chamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), o Gerenciador de e/s do driver verifica se o usuário fornecido tem o acesso necessário e, da mesma forma, o Access verifica quando os IOCTLs são enviados para o driver a partir desse identificador.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="5e5a0-107">Por exemplo, um administrador de rede pode restringir os usuários convidados a acesso somente leitura para dispositivos portáteis, enquanto eles poderiam conceder aos usuários autenticados acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="5e5a0-108">Nesse caso, isso significa que, se um convidado emitisse um comando WPD que exigia acesso de leitura/gravação (como Delete Object); Ele falharia com acesso negado, enquanto que um usuário autenticado emitiu o mesmo comando, ele teria êxito.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="5e5a0-109">As entradas de Política de Grupo para controlar o acesso ao armazenamento removível e aos dispositivos portáteis não são, na verdade, nada mais do que uma maneira fácil de os administradores aplicarem ACLs de nó de dispositivo PnP a uma classe inteira de dispositivos de cada vez (por exemplo, aplicar a permissão "negar acesso de gravação a dispositivos portáteis Política de Grupo" ajustaria as ACLs de todos os dispositivos WPD para negar acesso de gravação</span><span class="sxs-lookup"><span data-stu-id="5e5a0-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="5e5a0-110">Códigos de controle de e/s em WPD</span><span class="sxs-lookup"><span data-stu-id="5e5a0-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="5e5a0-111">Aplicativos WPD se comunicam com drivers abrindo identificadores de dispositivo e enviando códigos de controle de e/s (IOCTLs).</span><span class="sxs-lookup"><span data-stu-id="5e5a0-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="5e5a0-112">Esses IOCTLs consistem em quatro seções:</span><span class="sxs-lookup"><span data-stu-id="5e5a0-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="5e5a0-113">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5e5a0-113">Device Type</span></span>
2.  <span data-ttu-id="5e5a0-114">Código de função</span><span class="sxs-lookup"><span data-stu-id="5e5a0-114">Function Code</span></span>
3.  <span data-ttu-id="5e5a0-115">Método de buffer</span><span class="sxs-lookup"><span data-stu-id="5e5a0-115">Buffer Method</span></span>
4.  <span data-ttu-id="5e5a0-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5e5a0-116">Access Type</span></span>

<span data-ttu-id="5e5a0-117">A quarta seção, o tipo de acesso, especifica o requisito de acesso específico para o comando fornecido.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="5e5a0-118">O Gerenciador de e/s do driver usa esses dados para executar a verificação da ACL (lista de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="5e5a0-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="5e5a0-119">Portanto, se um IOCTL foi definido como:</span><span class="sxs-lookup"><span data-stu-id="5e5a0-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="5e5a0-120">O Gerenciador de e/s do driver verificaria se o proprietário do identificador do dispositivo tem acesso de leitura ao dispositivo quando essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="5e5a0-121">E, se um IOCTL foi definido como:</span><span class="sxs-lookup"><span data-stu-id="5e5a0-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="5e5a0-122">O Gerenciador de e/s do driver verificaria se o proprietário do identificador do dispositivo tem acesso de leitura/gravação ao dispositivo quando essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="5e5a0-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e5a0-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e5a0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e5a0-124">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="5e5a0-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="5e5a0-125">**IPortableDevice:: abrir**</span><span class="sxs-lookup"><span data-stu-id="5e5a0-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="5e5a0-126">**IPortableDevice::SendCommand**</span><span class="sxs-lookup"><span data-stu-id="5e5a0-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



