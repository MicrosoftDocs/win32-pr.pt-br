---
description: Representa as informações mantidas no Gerenciador de partições sobre um disco que faz parte de um cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Estrutura de DISK_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753484"
---
# <a name="disk_cluster_info-structure"></a>Estrutura de informações de \_ cluster de disco \_

Representa as informações mantidas no Gerenciador de partições sobre um disco que faz parte de um cluster.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

O número de versão. Esse valor deve ser definido como o tamanho dessa estrutura.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Uma combinação de sinalizadores relacionados a discos e clusters.



| Valor                                                                                                                                                                                                                                                                                               | Significado                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**Disco \_ Sinalizador de CLUSTER \_ \_ habilitado**</dt> <dt>1</dt> </dl>                                          | O disco é usado como parte do serviço de cluster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**Disco \_ Sinalizador de CLUSTER \_ \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Os volumes no disco são expostos por CSVFS em todos os nós do cluster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**Disco \_ \_Sinalizador \_ de cluster em \_ manutenção**</dt> <dt>4</dt> </dl>                    | O recurso de cluster associado a este disco está em modo de manutenção.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**Disco \_ A chegada de PnP do sinalizador de CLUSTER foi \_ \_ \_ \_ concluída**</dt> <dt>8</dt> </dl> | O driver de disco de cluster para o modo kernel (Clusdisk) recebeu uma notificação PnP da chegada do disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Os sinalizadores que estão sendo modificados no membro **flags** .

</dd> <dt>

**Notificar**
</dt> <dd>

**True** para enviar uma notificação de alteração de layout; caso contrário, **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de gerenciamento de disco](disk-management-structures.md)
</dt> <dt>

[**\_informações do \_ cluster de obtenção de disco de IOCTL \_ \_**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**\_informações do \_ cluster do conjunto de discos do IOCTL \_ \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




