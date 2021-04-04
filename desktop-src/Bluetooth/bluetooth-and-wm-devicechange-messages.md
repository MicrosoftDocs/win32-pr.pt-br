---
title: Mensagens de WM_DEVICECHANGE e Bluetooth
description: O Bluetooth inclui mensagens específicas do DEVICECHANGE do WM \_ que permitem aos desenvolvedores obter mensagens quando os dispositivos Bluetooth sofrerem alterações de status.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917391"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="686f8-103">Mensagens DEVICECHANGE do Bluetooth e do WM \_</span><span class="sxs-lookup"><span data-stu-id="686f8-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="686f8-104">O Bluetooth inclui mensagens específicas do [**\_ DEVICECHANGE do WM**](/windows/desktop/DevIO/wm-devicechange) que permitem aos desenvolvedores obter mensagens quando os dispositivos Bluetooth sofrerem alterações de status.</span><span class="sxs-lookup"><span data-stu-id="686f8-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="686f8-105">Este tópico descreve como receber mensagens **\_ DEVICECHANGE do WM** específicas do Bluetooth e lista mensagens específicas do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="686f8-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="686f8-106">Recebendo mensagens DEVICECHANGE do WM específicas do Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="686f8-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="686f8-107">Para receber mensagens do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , primeiro é necessário abrir um identificador para o rádio local.</span><span class="sxs-lookup"><span data-stu-id="686f8-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="686f8-108">Para tal, use um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="686f8-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="686f8-109">Use a função [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) com os seguintes parâmetros: (GUID \_ BTHPORT \_ Device \_ interface,..., DIGCF \_ presente \| DIGCF \_ DEVICEINTERFACE) e, em seguida, use as funções [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .</span><span class="sxs-lookup"><span data-stu-id="686f8-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="686f8-110">Use as funções [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .</span><span class="sxs-lookup"><span data-stu-id="686f8-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="686f8-111">Quando o identificador de rádio Bluetooth for aberto, chame a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registre-se para obter notificações sobre o identificador usando **DBT \_ DEVTYP \_ Handle** como o DeviceType.</span><span class="sxs-lookup"><span data-stu-id="686f8-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="686f8-112">Quando registrado, os GUIDs a seguir são enviados e o membro de [**transmissão do dev \_ \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_ Data** member é o buffer associado.</span><span class="sxs-lookup"><span data-stu-id="686f8-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="686f8-113">Mensagens específicas do Bluetooth</span><span class="sxs-lookup"><span data-stu-id="686f8-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="686f8-114">A tabela a seguir lista as mensagens [**\_ DEVICECHANGE do WM**](/windows/desktop/DevIO/wm-devicechange) específicas do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="686f8-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="686f8-115">GUID</span><span class="sxs-lookup"><span data-stu-id="686f8-115">GUID</span></span>                                   | <span data-ttu-id="686f8-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="686f8-116">BUFFER</span></span>                                                  | <span data-ttu-id="686f8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="686f8-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686f8-118">\_evento de \_ HCI do Bluetooth do GUID \_</span><span class="sxs-lookup"><span data-stu-id="686f8-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="686f8-119">**\_informações do \_ evento BTH HCI \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="686f8-120">Essa mensagem é enviada quando um dispositivo Bluetooth remoto se conecta ou se desconecta no nível de ACL.</span><span class="sxs-lookup"><span data-stu-id="686f8-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="686f8-121">\_ \_ Evento L2CAP de Bluetooth de GUID \_</span><span class="sxs-lookup"><span data-stu-id="686f8-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="686f8-122">**\_Informações do \_ evento BTH L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="686f8-123">Essa mensagem é enviada quando um canal L2CAP entre o rádio local e um dispositivo Bluetooth remoto foi estabelecido ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="686f8-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="686f8-124">Para canais L2CAP que são multiplexadores, como RFCOMM, essa mensagem é enviada somente quando o canal subjacente é estabelecido, não quando cada canal multiplexado, como um canal de RFCOMM, é estabelecido ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="686f8-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="686f8-125">\_solicitação de \_ PIN de Bluetooth de GUID \_</span><span class="sxs-lookup"><span data-stu-id="686f8-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="686f8-126">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="686f8-126">Not applicable.</span></span>                                         | <span data-ttu-id="686f8-127">Essa mensagem deve ser ignorada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="686f8-127">This message should be ignored by the application.</span></span> <span data-ttu-id="686f8-128">Se o aplicativo precisar receber solicitações de PIN, a função [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) deverá ser usada.</span><span class="sxs-lookup"><span data-stu-id="686f8-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="686f8-129">\_rádio Bluetooth \_ \_ de GUID no \_ intervalo</span><span class="sxs-lookup"><span data-stu-id="686f8-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="686f8-130">**\_rádio BTH \_ no \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="686f8-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="686f8-131">Essa mensagem é enviada quando qualquer um dos seguintes atributos de um dispositivo Bluetooth remoto foi alterado: o dispositivo foi descoberto, a classe de dispositivo, o nome, o estado conectado ou o estado memorizado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="686f8-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="686f8-132">Essa mensagem também é enviada quando esses atributos são definidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="686f8-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="686f8-133">\_rádio Bluetooth \_ \_ de GUID fora \_ do \_ intervalo</span><span class="sxs-lookup"><span data-stu-id="686f8-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="686f8-134">**\_endereço Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="686f8-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="686f8-135">Essa mensagem é enviada quando um dispositivo descoberto anteriormente não foi encontrado após a conclusão da última consulta.</span><span class="sxs-lookup"><span data-stu-id="686f8-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="686f8-136">Esta mensagem não será enviada para dispositivos lembrados.</span><span class="sxs-lookup"><span data-stu-id="686f8-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="686f8-137">A estrutura de **\_ endereço BTH** é o endereço do dispositivo que não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="686f8-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="686f8-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="686f8-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="686f8-139">**BluetoothFindFirstRadio**</span><span class="sxs-lookup"><span data-stu-id="686f8-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="686f8-140">**BluetoothFindNextRadio**</span><span class="sxs-lookup"><span data-stu-id="686f8-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="686f8-141">**BluetoothFindRadioClose**</span><span class="sxs-lookup"><span data-stu-id="686f8-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="686f8-142">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="686f8-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="686f8-143">SetupDiDestroyDeviceInfoList</span><span class="sxs-lookup"><span data-stu-id="686f8-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="686f8-144">SetupDiEnumDeviceInterfaces</span><span class="sxs-lookup"><span data-stu-id="686f8-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="686f8-145">SetupDiGetClassDevs</span><span class="sxs-lookup"><span data-stu-id="686f8-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="686f8-146">**\_endereço Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="686f8-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="686f8-147">**\_informações do \_ evento BTH HCI \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="686f8-148">**\_Informações do \_ evento BTH L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="686f8-149">**\_rádio BTH \_ no \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="686f8-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="686f8-150">**\_identificador de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="686f8-151">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="686f8-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 