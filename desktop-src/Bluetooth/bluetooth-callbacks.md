---
title: Retornos de chamada Bluetooth
description: As funções de retorno de chamada do Bluetooth nesta seção são usadas em combinação com funções que possibilitam o gerenciamento de dispositivos e serviços Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635106"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="7f3b3-103">Retornos de chamada Bluetooth</span><span class="sxs-lookup"><span data-stu-id="7f3b3-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="7f3b3-104">As funções de retorno de chamada do Bluetooth nesta seção são usadas em combinação com funções que possibilitam o gerenciamento de dispositivos e serviços Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="7f3b3-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="7f3b3-105">O Bluetooth também tem suporte usando a interface de programação do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="7f3b3-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="7f3b3-106">Para obter mais informações sobre como programar o Bluetooth usando a interface do Windows Sockets, consulte [suporte do Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="7f3b3-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="7f3b3-107">Seção</span><span class="sxs-lookup"><span data-stu-id="7f3b3-107">Section</span></span>                                                                                      | <span data-ttu-id="7f3b3-108">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="7f3b3-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f3b3-109">**retorno de chamada de \_ autenticação PFN \_**</span><span class="sxs-lookup"><span data-stu-id="7f3b3-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="7f3b3-110">Usado em conjunto com a função [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="7f3b3-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="7f3b3-111">**\_retorno de chamada de autenticação PFN \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="7f3b3-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="7f3b3-112">Usado em conjunto com a função [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .</span><span class="sxs-lookup"><span data-stu-id="7f3b3-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="7f3b3-113">**\_retorno de \_ \_ chamada de atributos de enumeração Bluetooth PFN \_**</span><span class="sxs-lookup"><span data-stu-id="7f3b3-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="7f3b3-114">Chamado uma vez para cada atributo encontrado no parâmetro *pSDPStream* que é passado para a chamada de função [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) .</span><span class="sxs-lookup"><span data-stu-id="7f3b3-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="7f3b3-115">**retorno de chamada do \_ dispositivo PFN \_**</span><span class="sxs-lookup"><span data-stu-id="7f3b3-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="7f3b3-116">Usado em associação com a seleção de dispositivos Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="7f3b3-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




