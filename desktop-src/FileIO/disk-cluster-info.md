---
description: Representa informações mantidas no gerenciador de partições sobre um disco que faz parte de um cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: DISK_CLUSTER_INFO (Ntdddisk.h)
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
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813788"
---
# <a name="disk_cluster_info-structure"></a>Estrutura DE \_ INFORMAÇÕES DO CLUSTER DE \_ DISCO

Representa informações mantidas no gerenciador de partições sobre um disco que faz parte de um cluster.

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
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**DISCO \_ SINALIZADOR \_ DE CLUSTER \_ HABILITADO**</dt> <dt>1</dt> </dl>                                          | O disco é usado como parte do serviço de cluster.<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**DISCO \_ SINALIZADOR \_ DE CLUSTER \_ CSV**</dt> <dt>2</dt> </dl>                                                      | Os volumes no disco são expostos pelo CSVFS em todos os nós do cluster.<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**DISCO \_ SINALIZADOR \_ DE CLUSTER NA \_ \_ MANUTENÇÃO**</dt> <dt>4</dt> </dl>                    | O recurso de cluster associado a esse disco está no modo de manutenção.<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**DISCO \_ CLUSTER \_ FLAG \_ PNP ARRIVAL \_ \_ COMPLETE**</dt> <dt>8</dt> </dl> | O driver de disco de cluster para o modo kernel (clusdisk) recebeu notificação pnP da chegada do disco.<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

Os sinalizadores que estão sendo modificados no **membro Flags.**

</dd> <dt>

**Notificar**
</dt> <dd>

**TRUE** para enviar uma notificação de alteração de layout; caso contrário, **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de gerenciamento de disco](disk-management-structures.md)
</dt> <dt>

[**INFORMAÇÕES DE \_ CLUSTER DE GET \_ DO \_ \_ DISCO IOCTL**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**INFORMAÇÕES DE CLUSTER DO CONJUNTO \_ DE \_ DISCOS \_ IOCTL \_**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




