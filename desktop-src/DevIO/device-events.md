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
# <a name="device-events-ioeventh"></a>Eventos de dispositivo (IoEvent. h)

Aplicativos, incluindo serviços, podem se registrar para receber notificações de eventos de dispositivo. Por exemplo, um serviço de catálogo pode receber um aviso de volumes sendo montados ou desmontados para que possa ajustar os caminhos para arquivos no volume. O sistema notifica um aplicativo de que ocorreu um evento de dispositivo enviando o aplicativo a uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) . O sistema notifica um serviço de que um evento de dispositivo ocorreu invocando a função do manipulador de eventos do serviço, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Para receber avisos de eventos de dispositivo, chame a função [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) com uma estrutura de [**identificador de \_ difusão \_ de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) . Certifique-se de definir o membro do **\_ identificador dbch** para o identificador do dispositivo obtido da função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Além disso, defina o membro **dbch \_ DeviceType** como **DBT \_ DEVTYP \_ Handle**. A função retorna um identificador de notificação de dispositivo. Observe que isso não é o mesmo que o identificador de volume.

Quando seu aplicativo receber notificação, se o tipo de evento for [DBT \_ CUSTOMEVENT](dbt-customevent.md), você poderá ter recebido um dos eventos de dispositivo definidos em IoEvent. h. Para determinar se um desses eventos ocorreu, use as etapas a seguir.

1.  Trate os dados de evento como uma estrutura [**\_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Verifique se o membro **dbch \_ DeviceType** está definido como **DBT \_ DEVTYP \_ Handle**.
2.  Se **dbch \_ DeviceType** for **DBT \_ DEVTYP \_ Handle**, os dados do evento serão, na verdade, um ponteiro para uma estrutura de [**\_ \_ identificador de difusão de desenvolvimento**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .
3.  Compare o membro **dbch \_ EventGuid** ao **GUID** s listado na tabela a seguir usando a função [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID de \_ e/s de \_ ROM de \_ \_ bloqueio exclusivo**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



O dispositivo de CD-ROM foi bloqueado para acesso exclusivo.

**Windows Server 2003 e Windows XP:** O suporte para esse valor requer o IMAPi 2,0. Para obter mais informações, consulte [API de mestre de imagem](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_desbloqueio \_ exclusivo de cdrom Io \_ de GUID \_**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Um dispositivo de CD-ROM que foi bloqueado para acesso exclusivo foi desbloqueado.

**Windows Server 2003 e Windows XP:** O suporte para esse valor requer o IMAPi 2,0. Para obter mais informações, consulte [API de mestre de imagem](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**o \_ dispositivo de e/s de GUID \_ \_ \_ está se preparando**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A rotação de mídia está em andamento.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ solicitação externa do dispositivo e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Há várias causas possíveis para esse evento; para obter mais informações, consulte a especificação do MMC do T10 do comando obter notificação de STATUS de evento, em [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_chegada de mídia de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A mídia removível foi adicionada ao dispositivo. O membro de **\_ dados dbch** é um ponteiro para uma estrutura de [**contexto de alteração de mídia de classe \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . O membro **NewState** fornece informações de status. Por exemplo, um valor de **MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de registro ativa).

**Windows XP:** O membro de **\_ dados dbch** é um valor **ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_solicitação de \_ ejeção de mídia de e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A unidade da mídia removível recebeu uma solicitação do usuário para ejetar o slot ou a mídia especificada.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_remoção de mídia de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A mídia removível foi removida do dispositivo ou está indisponível. O membro de **\_ dados dbch** é um ponteiro para uma estrutura de [**contexto de alteração de mídia de classe \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . O membro **NewState** fornece informações de status. Por exemplo, um valor de **MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de registro ativa).

**Windows XP:** O membro de **\_ dados dbch** é um valor **ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_alteração de \_ volume de es de GUID \_**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



O rótulo do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_tamanho da \_ alteração do volume de e/s do \_ GUID \_**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



O tamanho do sistema de arquivos no volume foi alterado.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**desmontagem de \_ volume de e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Uma tentativa de desmontar o volume está em andamento. Você deve fechar todos os identificadores para arquivos e diretórios no volume. Esse evento não será necessariamente precedido por um evento **de \_ \_ \_ bloqueio de volume de e/s de GUID** .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ \_ falha ao desmontar volume de e/s de GUID \_**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Falha ao tentar desmontar um volume. Isso geralmente acontece porque outro processo não respondeu a um aviso **de \_ \_ \_ desmontagem de volume de e/s de GUID** fechando seus identificadores pendentes. Como a desmontagem falhou, você pode reabrir quaisquer identificadores para o volume afetado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_alteração de \_ status de FVE de volume de es GUID \_ \_ \_**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



O status de Criptografia de Unidade de Disco BitLocker do volume foi alterado. Esse evento é sinalizado quando o BitLocker é habilitado ou desabilitado, ou quando a criptografia começa, termina, pausa ou retoma.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_bloqueio de volume de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

50708874-c9af-11D1-8FEF-00a0c9a06d32
</dt> <dt>



Outro processo está tentando bloquear o volume. Você deve fechar todos os identificadores para arquivos e diretórios no volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_ \_ \_ falha no bloqueio de volume de es de GUID \_**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Falha ao tentar bloquear um volume. Isso geralmente acontece porque outro processo não respondeu a um evento **de \_ \_ \_ bloqueio de volume de e/s GUID** fechando seus identificadores pendentes. Como o bloqueio falhou, você pode reabrir quaisquer identificadores para o volume afetado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montagem de volume de e/s de GUID \_ \_**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



O volume foi montado por outro processo. Você pode abrir um ou mais identificadores para ele.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_alteração de \_ nome de volume de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



O nome do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**o \_ volume de e/s de GUID \_ \_ precisa de \_ chkdsk**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Um sistema de arquivos detectou corrupção no volume. O aplicativo deve executar CHKDSK no volume ou notificar o usuário para fazer isso.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_alteração de \_ \_ configuração física \_ do volume de e/s de GUID \_**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



A composição física ou o estado físico atual do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**fim \_ da \_ preparação do volume de e/s de \_ GUID \_**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



O sistema de arquivos está preparando o disco para ser ejetado. Por exemplo, o sistema de arquivos está parando uma operação de formatação em segundo plano ou fechando a sessão na mídia de gravação única.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_alteração de \_ \_ ID exclusiva \_ de volume de e/s de GUID \_**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



O identificador exclusivo do volume foi alterado. Para obter mais informações sobre o identificador exclusivo, [**consulte \_ \_ \_ \_ ID exclusiva da consulta MOUNTDEV do IOCTL**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Server 2008 R2 e o Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**desbloqueio de \_ volume de e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



O volume foi desbloqueado por outro processo. Você pode abrir um ou mais identificadores para ele.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**\_volume de e/s de GUID \_ \_ desgastando \_**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



A mídia está se desgastando. Esse evento é enviado quando um sistema de arquivos determina que a taxa de erros em um volume é muito alta ou seu espaço de substituição de defeito está quase esgotado.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os eventos de **\_ \_ \_ \_ falha** de desmontagem de volume de e/s de GUID e desmontagem de volume do GUID são relacionados, assim como o evento de **\_ \_ \_ \_ falha de bloqueio** de volume de e/s de **GUID \_ \_ \_** e a es **\_ \_ \_** Os eventos de **\_ \_ \_ bloqueio** de volume de e/s do **GUID de \_ \_ \_ desmontagem** e GUID indicam que uma operação está sendo tentada. Você deve agir sobre a notificação de eventos e registrar a ação executada. **Falha na \_ \_ \_ desmontagem do \_ volume** de e/s de GUID e eventos de **\_ \_ \_ \_ falha de bloqueio de volume de es de GUID** indicam que a operação tentada falhou. Em seguida, você pode usar o registro para desfazer as ações feitas em resposta à operação.

O membro **dbch \_ hdevnotify** da estrutura [**do \_ \_ identificador de difusão de desenvolvimento**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica o dispositivo afetado. Observe que esse é o identificador de notificação do dispositivo retornado por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), não como um identificador de volume. Para executar operações no volume, mapeie esse identificador para o identificador de volume correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>IoEvent. h</dt> </dl> |



 

