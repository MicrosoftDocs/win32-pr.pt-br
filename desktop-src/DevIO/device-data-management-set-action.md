---
description: Defina o conjunto de ações para o \_ código de \_ controle gerenciar atributos de conjunto de dados de armazenamento de IOCTL \_ \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826382"
---
# <a name="device_data_management_set_action"></a>\_ação do \_ conjunto de gerenciamento de dados do dispositivo \_ \_

Os valores constantes a seguir são o conjunto de valores possíveis para o tipo de ação do conjunto de gerenciamento de dados do dispositivo, que é definido como o tipo **DWORD**. **\_ \_ \_ \_**

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ nenhum**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Nenhuma ação é executada.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Uma ação de corte é executada.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Notificação de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000002)
</dt> <dt>



Uma ação de notificação é executada. Os parâmetros estão em uma estrutura de [**parâmetros de notificação do DSM do dispositivo \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) . O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000003)
</dt> <dt>



Uma ação de leitura de descarregamento é executada. Os parâmetros estão em uma estrutura de [**\_ parâmetros de \_ \_ leitura \_ de descarregamento de DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . A saída está em uma estrutura de [**\_ saída de \_ leitura \_ de descarregamento de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) . O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Uma ação de gravação de descarregamento é executada. Os parâmetros estão em uma estrutura de [**\_ parâmetros de \_ \_ gravação \_ de descarregamento de DSM de dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) . A saída está em uma estrutura de [**\_ saída de \_ gravação \_ de descarregamento de armazenamento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Alocação de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000005)
</dt> <dt>



Um bitmap de alocação é retornado para o primeiro intervalo de conjuntos de dados passado. A saída está em uma estrutura de [**estado de provisionamento do conjunto de dados de dispositivo \_ \_ \_ lb \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) . O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Reparo DeviceDsmAction**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000006)
</dt> <dt>



Uma ação de reparo é executada. O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**Limpeza de DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000007)
</dt> <dt>



Uma ação de limpeza é executada. O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Resiliência DeviceDsmAction**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag não \_ destrutivos** (0x80000008)
</dt> <dt>



Uma ação de resiliência é executada. O **DeviceDsmActionFlag não \_ destrutivo** (0x80000000) é um sinalizador de bit para indicar à pilha de drivers que essa operação não é destrutiva.

**Windows 7 e Windows Server 2008 R2:** Esse valor não tem suporte antes do Windows 8 e do Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                                         |
| parâmetro<br/>                   | <dl> <dt>WinIoCtl. h (incluir Windows. h)</dt> </dl> |



 

 




