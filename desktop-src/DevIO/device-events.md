---
description: Aplicativos, incluindo serviços, podem se registrar para receber notificação de eventos do dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventos de dispositivo (IoEvent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44e6160ef3a59821e5d2b2a3d4e42ee1d14d5c2fb7deda689fb1c9c3186b428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076250"
---
# <a name="device-events-ioeventh"></a>Eventos de dispositivo (IoEvent.h)

Aplicativos, incluindo serviços, podem se registrar para receber notificação de eventos do dispositivo. Por exemplo, um serviço de catálogo pode receber avisos de volumes sendo montados ou desmontados para que ele possa ajustar os caminhos para arquivos no volume. O sistema notifica um aplicativo de que ocorreu um evento de dispositivo enviando ao aplicativo uma mensagem [**WM \_ DEVICECHANGE.**](wm-devicechange.md) O sistema notifica um serviço de que ocorreu um evento de dispositivo invocando a função de manipulador de eventos do serviço, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Para receber avisos de evento do dispositivo, chame a [**função RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) com uma estrutura [**DEV \_ BROADCAST \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) Certifique-se de definir **o membro do dbch \_ handle** como o alça do dispositivo obtido da [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Além disso, de definido **o membro \_ dbch devicetype** como **DBT \_ DEVTYP \_ HANDLE**. A função retorna um alça de notificação do dispositivo. Observe que isso não é o mesmo que o alça de volume.

Quando seu aplicativo receber notificação, se o tipo de evento for [DBT \_ CUSTOMEVENT](dbt-customevent.md), você poderá ter recebido um dos eventos de dispositivo definidos em IoEvent.h. Para determinar se um desses eventos ocorreu, use as etapas a seguir.

1.  Trate os dados do evento como uma estrutura [**\_ \_ HDR DEV BROADCAST.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Verifique se o **membro dbch \_ devicetype** está definido como **DBT \_ DEVTYP \_ HANDLE**.
2.  Se **dbch \_ devicetype** for **DBT \_ DEVTYP \_ HANDLE**, os dados do evento serão realmente um ponteiro para uma estrutura [**DEV \_ BROADCAST \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)
3.  Compare o **membro dbch \_ eventguid** com **os GUID** listados na tabela a seguir usando a [**função IsEqualGUID.**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO \_ CDROM \_ EXCLUSIVE \_ LOCK**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



O dispositivo CD-ROM foi bloqueado para acesso exclusivo.

**Windows Server 2003 e Windows XP:** O suporte para esse valor requer IMAPI 2.0. Para obter mais informações, consulte [API de Controle de Imagem](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ CDROM \_ EXCLUSIVE \_ UNLOCK**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Um dispositivo CD-ROM bloqueado para acesso exclusivo foi desbloqueado.

**Windows Server 2003 e Windows XP:** O suporte para esse valor requer IMAPI 2.0. Para obter mais informações, consulte [API de Controle de Imagem](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**DISPOSITIVO \_ DE \_ E/S GUID SE \_ PREPARANDO \_**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A rotação de mídia está em andamento.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**SOLICITAÇÃO EXTERNA DO DISPOSITIVO \_ DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Há várias causas possíveis para esse evento; Para obter mais informações, consulte a especificação T10 MMC do comando GET EVENT STATUS NOTIFICATION, em [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**CHEGADA \_ DA MÍDIA DE E/S \_ \_ GUID**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A mídia removível foi adicionada ao dispositivo. O **membro \_ de dados dbch** é um ponteiro para uma estrutura [**CLASS MEDIA CHANGE \_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) O **membro NewState** fornece informações de status. Por exemplo, um valor **de MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de gravação ativa).

**Windows XP:** O **membro de \_ dados dbch** é **um valor ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**SOLICITAÇÃO \_ DE EJETO DE MÍDIA DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A unidade da mídia removível recebeu uma solicitação do usuário para ejetar o slot ou a mídia especificado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**REMOÇÃO \_ DE MÍDIA DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



A mídia removível foi removida do dispositivo ou não está disponível. O **membro \_ de dados dbch** é um ponteiro para uma estrutura [**CLASS MEDIA CHANGE \_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) O **membro NewState** fornece informações de status. Por exemplo, um valor **de MediaUnavailable** indica que a mídia não está disponível (por exemplo, devido a uma sessão de gravação ativa).

**Windows XP:** O **membro de \_ dados dbch** é **um valor ULONG** que representa o número de vezes que a mídia foi alterada desde a inicialização do sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**ALTERAÇÃO \_ DE VOLUME DE E/S \_ \_ GUID**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



O rótulo do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**TAMANHO \_ DA ALTERAÇÃO DO VOLUME DE \_ \_ E/S DO \_ GUID**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



O tamanho do sistema de arquivos no volume foi alterado.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**DESMONTAGEM \_ DE VOLUME DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Uma tentativa de desmontar o volume está em andamento. Você deve fechar todos os alças para arquivos e diretórios no volume. Esse evento não será necessariamente precedido por um **evento GUID \_ E/S \_ VOLUME \_ LOCK.**


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**FALHA \_ NA DESMONTAGEM DO \_ VOLUME DE \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Falha ao tentar desmontar um volume. Isso geralmente acontece porque outro processo não respondeu a um **aviso DE \_ \_ \_ DESMONTAGEM** DE VOLUME de E/S GUID fechando seus alças pendentes. Como a desmontagem falhou, você pode reabrir quaisquer alças para o volume afetado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**ALTERAÇÃO DE STATUS \_ \_ DE FVE DE VOLUME DE \_ \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



O status de Criptografia de Unidade de Disco BitLocker do volume foi alterado. Esse evento é sinalizado quando o BitLocker está habilitado ou desabilitado ou quando a criptografia começa, termina, pausa ou é retomada.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ \_ E/S VOLUME \_ LOCK**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



Outro processo é tentar bloquear o volume. Você deve fechar todos os alças para arquivos e diretórios no volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**FALHA NO \_ BLOQUEIO DE VOLUME DE E/S \_ \_ \_ GUID**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Falha ao tentar bloquear um volume. Isso geralmente acontece porque outro processo falhou ao responder a um **evento GUID \_ E/S \_ VOLUME \_ LOCK** fechando seus alças pendentes. Como o bloqueio falhou, você pode reabrir quaisquer alças para o volume afetado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**MONTAGEM \_ DE VOLUME DE \_ E/S \_ GUID**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



O volume foi montado por outro processo. Você pode abrir um ou mais alças para ele.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**ALTERAÇÃO \_ DO NOME DO VOLUME DE \_ \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



O nome do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**O VOLUME \_ DE \_ E/S GUID PRECISA DE \_ \_ CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Um sistema de arquivos detectou corrupção no volume. O aplicativo deve executar CHKDSK no volume ou notificar o usuário para fazer isso.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**ALTERAÇÃO NA \_ CONFIGURAÇÃO FÍSICA \_ DO VOLUME DE \_ \_ \_ E/S GUID**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



O estado físico físico ou o estado físico atual do volume foi alterado.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_EJETAR PREPARAÇÃO DO VOLUME DE E/S \_ \_ \_ GUID**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



O sistema de arquivos está preparando o disco a ser ejetado. Por exemplo, o sistema de arquivos está interrompendo uma operação de formatação em segundo plano ou fechando a sessão na mídia de gravação única.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**ALTERAÇÃO DE ID EXCLUSIVA DO \_ \_ VOLUME DE \_ \_ \_ E/S DO GUID**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



O identificador exclusivo do volume foi alterado. Para obter mais informações sobre o identificador exclusivo, confira [**IOCTL \_ MOUNTDEV \_ QUERY \_ UNIQUE \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Esse valor não tem suporte até Windows Server 2008 R2 e Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ E/S \_ VOLUME \_ UNLOCK**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



O volume foi desbloqueado por outro processo. Você pode abrir um ou mais alças para ele.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**VOLUME \_ DE \_ E/S GUID \_ \_ DESEMOCAR**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaaaa
</dt> <dt>



A mídia está desem uniforme. Esse evento é enviado quando um sistema de arquivos determina que a taxa de erro em um volume é muito alta ou seu espaço de substituição de defeito está quase esgotado.

**Windows Server 2003 e Windows XP:** Não há suporte para esse valor.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os **eventos GUID \_ IO VOLUME \_ \_ DISMOUNT** e **GUID \_ IO VOLUME \_ \_ DISMOUNT \_ FAILED** estão relacionados, assim como o **evento GUID \_ IO VOLUME \_ \_ LOCK** e **GUID \_ IO VOLUME LOCK \_ \_ \_ FAILED.** Os **eventos GUID \_ IO VOLUME \_ \_ DISMOUNT** e **GUID \_ IO VOLUME \_ \_ LOCK** indicam que uma operação está sendo tentada. Você deve agir na notificação de eventos e registrar a ação tomada. Os **eventos GUID \_ IO VOLUME \_ \_ DISMOUNT \_ FAILED** e **GUID \_ IO VOLUME LOCK \_ \_ \_ FAILED** indicam que a tentativa de operação falhou. Em seguida, você pode usar seu registro para desfazer as ações feitas em resposta à operação.

O **membro dbch \_ hdevnotify** da estrutura [**DEV BROADCAST \_ \_ HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica o dispositivo afetado. Observe que esse é o handle de notificação do dispositivo retornado por [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), não um alça de volume. Para executar operações no volume, mapeie esse alça para o alça de volume correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>IoEvent.h</dt> </dl> |



 

