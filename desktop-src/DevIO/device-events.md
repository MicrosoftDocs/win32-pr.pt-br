---
description: Aplicativos, incluindo serviços, podem se registrar para receber notificações de eventos de dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventos de dispositivo (IoEvent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163896"
---
# <a name="device-events-ioeventh"></a><span data-ttu-id="44aef-103">Eventos de dispositivo (IoEvent. h)</span><span class="sxs-lookup"><span data-stu-id="44aef-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="44aef-104">Aplicativos, incluindo serviços, podem se registrar para receber notificações de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44aef-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="44aef-105">Por exemplo, um serviço de catálogo pode receber um aviso de volumes sendo montados ou desmontados para que possa ajustar os caminhos para arquivos no volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="44aef-106">O sistema notifica um aplicativo de que ocorreu um evento de dispositivo enviando o aplicativo a uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="44aef-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="44aef-107">O sistema notifica um serviço de que um evento de dispositivo ocorreu invocando a função do manipulador de eventos do serviço, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="44aef-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="44aef-108">Para receber avisos de eventos de dispositivo, chame a função [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) com uma estrutura de [**identificador de \_ difusão \_ de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="44aef-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="44aef-109">Certifique-se de definir o membro do **\_ identificador dbch** para o identificador do dispositivo obtido da função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="44aef-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="44aef-110">Além disso, defina o membro **dbch \_ DeviceType** como **DBT \_ DEVTYP \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="44aef-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="44aef-111">A função retorna um identificador de notificação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44aef-111">The function returns a device notification handle.</span></span> <span data-ttu-id="44aef-112">Observe que isso não é o mesmo que o identificador de volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="44aef-113">Quando seu aplicativo receber notificação, se o tipo de evento for [DBT \_ CUSTOMEVENT](dbt-customevent.md), você poderá ter recebido um dos eventos de dispositivo definidos em IoEvent. h.</span><span class="sxs-lookup"><span data-stu-id="44aef-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="44aef-114">Para determinar se um desses eventos ocorreu, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="44aef-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="44aef-115">Trate os dados de evento como uma estrutura [**\_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="44aef-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="44aef-116">Verifique se o membro **dbch \_ DeviceType** está definido como **DBT \_ DEVTYP \_ Handle**.</span><span class="sxs-lookup"><span data-stu-id="44aef-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="44aef-117">Se **dbch \_ DeviceType** for **DBT \_ DEVTYP \_ Handle**, os dados do evento serão, na verdade, um ponteiro para uma estrutura de [**\_ \_ identificador de difusão de desenvolvimento**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="44aef-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="44aef-118">Compare o membro **dbch \_ EventGuid** ao **GUID** s listado na tabela a seguir usando a função [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .</span><span class="sxs-lookup"><span data-stu-id="44aef-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="44aef-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID de \_ e/s de \_ ROM de \_ \_ bloqueio exclusivo**</span><span class="sxs-lookup"><span data-stu-id="44aef-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="44aef-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="44aef-121">O dispositivo de CD-ROM foi bloqueado para acesso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="44aef-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="44aef-122">**Windows Server 2003 e Windows XP:** O suporte para esse valor requer o IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="44aef-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="44aef-123">Para obter mais informações, consulte [API de mestre de imagem](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="44aef-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_desbloqueio \_ exclusivo de cdrom Io \_ de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="44aef-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="44aef-126">Um dispositivo de CD-ROM que foi bloqueado para acesso exclusivo foi desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="44aef-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="44aef-127">**Windows Server 2003 e Windows XP:** O suporte para esse valor requer o IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="44aef-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="44aef-128">Para obter mais informações, consulte [API de mestre de imagem](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="44aef-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**o \_ dispositivo de e/s de GUID \_ \_ \_ está se preparando**</span><span class="sxs-lookup"><span data-stu-id="44aef-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="44aef-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="44aef-131">A rotação de mídia está em andamento.</span><span class="sxs-lookup"><span data-stu-id="44aef-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ solicitação externa do dispositivo e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="44aef-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="44aef-134">Há várias causas possíveis para esse evento; para obter mais informações, consulte a especificação do MMC do T10 do comando obter notificação de STATUS de evento, em [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="44aef-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_chegada de mídia de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="44aef-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="44aef-137">A mídia removível foi adicionada ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44aef-137">Removable media has been added to the device.</span></span> <span data-ttu-id="44aef-138">O membro de **\_ dados dbch** é um ponteiro para uma estrutura de [**contexto de alteração de mídia de classe \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="44aef-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="44aef-139">O membro **NewState** fornece informações de status.</span><span class="sxs-lookup"><span data-stu-id="44aef-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="44aef-140">Por exemplo, um valor de **MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de registro ativa).</span><span class="sxs-lookup"><span data-stu-id="44aef-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="44aef-141">**Windows XP:** O membro de **\_ dados dbch** é um valor **ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="44aef-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_solicitação de \_ ejeção de mídia de e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="44aef-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="44aef-144">A unidade da mídia removível recebeu uma solicitação do usuário para ejetar o slot ou a mídia especificada.</span><span class="sxs-lookup"><span data-stu-id="44aef-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_remoção de mídia de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="44aef-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="44aef-147">A mídia removível foi removida do dispositivo ou está indisponível.</span><span class="sxs-lookup"><span data-stu-id="44aef-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="44aef-148">O membro de **\_ dados dbch** é um ponteiro para uma estrutura de [**contexto de alteração de mídia de classe \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="44aef-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="44aef-149">O membro **NewState** fornece informações de status.</span><span class="sxs-lookup"><span data-stu-id="44aef-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="44aef-150">Por exemplo, um valor de **MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de registro ativa).</span><span class="sxs-lookup"><span data-stu-id="44aef-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="44aef-151">**Windows XP:** O membro de **\_ dados dbch** é um valor **ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="44aef-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_alteração de \_ volume de es de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="44aef-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="44aef-154">O rótulo do volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_tamanho da \_ alteração do volume de e/s do \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="44aef-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="44aef-157">O tamanho do sistema de arquivos no volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="44aef-158">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="44aef-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**desmontagem de \_ volume de e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-161">Uma tentativa de desmontar o volume está em andamento.</span><span class="sxs-lookup"><span data-stu-id="44aef-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="44aef-162">Você deve fechar todos os identificadores para arquivos e diretórios no volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="44aef-163">Esse evento não será necessariamente precedido por um evento **de \_ \_ \_ bloqueio de volume de e/s de GUID** .</span><span class="sxs-lookup"><span data-stu-id="44aef-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ \_ falha ao desmontar volume de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-166">Falha ao tentar desmontar um volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="44aef-167">Isso geralmente acontece porque outro processo não respondeu a um aviso **de \_ \_ \_ desmontagem de volume de e/s de GUID** fechando seus identificadores pendentes.</span><span class="sxs-lookup"><span data-stu-id="44aef-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="44aef-168">Como a desmontagem falhou, você pode reabrir quaisquer identificadores para o volume afetado.</span><span class="sxs-lookup"><span data-stu-id="44aef-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_alteração de \_ status de FVE de volume de es GUID \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="44aef-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="44aef-171">O status de Criptografia de Unidade de Disco BitLocker do volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="44aef-172">Esse evento é sinalizado quando o BitLocker é habilitado ou desabilitado, ou quando a criptografia começa, termina, pausa ou retoma.</span><span class="sxs-lookup"><span data-stu-id="44aef-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="44aef-173">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="44aef-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_bloqueio de volume de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-175">50708874-c9af-11D1-8FEF-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-176">Outro processo está tentando bloquear o volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="44aef-177">Você deve fechar todos os identificadores para arquivos e diretórios no volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_ \_ \_ falha no bloqueio de volume de es de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-180">Falha ao tentar bloquear um volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="44aef-181">Isso geralmente acontece porque outro processo não respondeu a um evento **de \_ \_ \_ bloqueio de volume de e/s GUID** fechando seus identificadores pendentes.</span><span class="sxs-lookup"><span data-stu-id="44aef-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="44aef-182">Como o bloqueio falhou, você pode reabrir quaisquer identificadores para o volume afetado.</span><span class="sxs-lookup"><span data-stu-id="44aef-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montagem de volume de e/s de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-185">O volume foi montado por outro processo.</span><span class="sxs-lookup"><span data-stu-id="44aef-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="44aef-186">Você pode abrir um ou mais identificadores para ele.</span><span class="sxs-lookup"><span data-stu-id="44aef-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_alteração de \_ nome de volume de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="44aef-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="44aef-189">O nome do volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**o \_ volume de e/s de GUID \_ \_ precisa de \_ chkdsk**</span><span class="sxs-lookup"><span data-stu-id="44aef-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="44aef-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="44aef-192">Um sistema de arquivos detectou corrupção no volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="44aef-193">O aplicativo deve executar CHKDSK no volume ou notificar o usuário para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="44aef-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="44aef-194">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="44aef-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_alteração de \_ \_ configuração física \_ do volume de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="44aef-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="44aef-197">A composição física ou o estado físico atual do volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**fim \_ da \_ preparação do volume de e/s de \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="44aef-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="44aef-200">O sistema de arquivos está preparando o disco para ser ejetado.</span><span class="sxs-lookup"><span data-stu-id="44aef-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="44aef-201">Por exemplo, o sistema de arquivos está parando uma operação de formatação em segundo plano ou fechando a sessão na mídia de gravação única.</span><span class="sxs-lookup"><span data-stu-id="44aef-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="44aef-202">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="44aef-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_alteração de \_ \_ ID exclusiva \_ de volume de e/s de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="44aef-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="44aef-205">O identificador exclusivo do volume foi alterado.</span><span class="sxs-lookup"><span data-stu-id="44aef-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="44aef-206">Para obter mais informações sobre o identificador exclusivo, [**consulte \_ \_ \_ \_ ID exclusiva da consulta MOUNTDEV do IOCTL**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="44aef-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="44aef-207">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Server 2008 R2 e o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="44aef-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**desbloqueio de \_ volume de e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="44aef-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="44aef-210">O volume foi desbloqueado por outro processo.</span><span class="sxs-lookup"><span data-stu-id="44aef-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="44aef-211">Você pode abrir um ou mais identificadores para ele.</span><span class="sxs-lookup"><span data-stu-id="44aef-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44aef-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**\_volume de e/s de GUID \_ \_ desgastando \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44aef-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="44aef-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="44aef-214">A mídia está se desgastando. Esse evento é enviado quando um sistema de arquivos determina que a taxa de erros em um volume é muito alta ou seu espaço de substituição de defeito está quase esgotado.</span><span class="sxs-lookup"><span data-stu-id="44aef-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="44aef-215">**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="44aef-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44aef-216">Comentários</span><span class="sxs-lookup"><span data-stu-id="44aef-216">Remarks</span></span>

<span data-ttu-id="44aef-217">Os eventos de **\_ \_ \_ \_ falha** de desmontagem de volume de e/s de GUID e desmontagem de volume do GUID são relacionados, assim como o evento de **\_ \_ \_ \_ falha de bloqueio** de volume de e/s de **GUID \_ \_ \_** e a es **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44aef-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="44aef-218">Os eventos de **\_ \_ \_ bloqueio** de volume de e/s do **GUID de \_ \_ \_ desmontagem** e GUID indicam que uma operação está sendo tentada.</span><span class="sxs-lookup"><span data-stu-id="44aef-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="44aef-219">Você deve agir sobre a notificação de eventos e registrar a ação executada.</span><span class="sxs-lookup"><span data-stu-id="44aef-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="44aef-220">**Falha na \_ \_ \_ desmontagem do \_ volume** de e/s de GUID e eventos de **\_ \_ \_ \_ falha de bloqueio de volume de es de GUID** indicam que a operação tentada falhou.</span><span class="sxs-lookup"><span data-stu-id="44aef-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="44aef-221">Em seguida, você pode usar o registro para desfazer as ações feitas em resposta à operação.</span><span class="sxs-lookup"><span data-stu-id="44aef-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="44aef-222">O membro **dbch \_ hdevnotify** da estrutura [**do \_ \_ identificador de difusão de desenvolvimento**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica o dispositivo afetado.</span><span class="sxs-lookup"><span data-stu-id="44aef-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="44aef-223">Observe que esse é o identificador de notificação do dispositivo retornado por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), não como um identificador de volume.</span><span class="sxs-lookup"><span data-stu-id="44aef-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="44aef-224">Para executar operações no volume, mapeie esse identificador para o identificador de volume correspondente.</span><span class="sxs-lookup"><span data-stu-id="44aef-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="44aef-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44aef-225">Requirements</span></span>



| <span data-ttu-id="44aef-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="44aef-226">Requirement</span></span> | <span data-ttu-id="44aef-227">Valor</span><span class="sxs-lookup"><span data-stu-id="44aef-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44aef-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44aef-228">Minimum supported client</span></span><br/> | <span data-ttu-id="44aef-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44aef-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="44aef-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44aef-230">Minimum supported server</span></span><br/> | <span data-ttu-id="44aef-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44aef-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="44aef-232">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44aef-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="44aef-233"><dt>IoEvent. h</dt></span><span class="sxs-lookup"><span data-stu-id="44aef-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

