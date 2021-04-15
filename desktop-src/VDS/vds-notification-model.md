---
description: Notificações do VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notificações do VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104569448"
---
# <a name="vds-notifications"></a>Notificações do VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um provedor pode enviar uma notificação de eventos para o VDS, e o VDS pode, por sua vez, encaminhar a notificação para os aplicativos. O modelo de notificação usado pelo VDS é semelhante ao modelo de ponto de conexão usado por objetos COM.

O VDS gera notificações de serviço para eventos como uma atribuição de letra de unidade ou a chegada de um disco não alocado. Depois que o VDS aloca um disco para um provedor, o provedor é responsável por gerar as notificações associadas. A ilustração a seguir mostra as interfaces e os métodos usados no modelo de notificação do VDS.

![Diagrama que mostra a interface e os métodos (Advise, OnLoad e OnNotify) entre aplicativos, serviço de disco virtual e provedores de V D S.](images/vdsnotification.png)

Para receber notificações, o VDS registra sua interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) com o objeto Provider chamando o método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) e passando um ponteiro para a interface. Quando ocorre um evento de notificação, como a chegada de um novo volume ou unidade, o provedor passa a estrutura de notificação apropriada para o VDS como um parâmetro do método [**IVdsAdviseSink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

O processo é semelhante entre um aplicativo e um VDS. Especificamente, para receber notificações, um aplicativo registra sua interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) com o VDS chamando o método [**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) e passando um ponteiro para a interface. Quando o VDS recebe uma notificação de um provedor, ele passa a estrutura de notificação apropriada para aplicativos registrados como um parâmetro do método [**IVdsAdviseSink:: OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

> [!Note]  
> Um aplicativo que chama [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) deve eventualmente chamar o método [**IVdsService:: Unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) . Idealmente, ele deve chamar **Unadvise** assim que não precisar mais receber notificações.

 

A tabela a seguir lista as notificações geradas pelo provedor por tipo de objeto.



| Objeto     | Notificação                              | Valor | Link para a descrição do evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **chegada do VDS \_ NF \_ Pack \_**                 | 1     | [**notificação do VDS \_ Pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **desparte do VDS \_ NF \_ Pack \_**                 | 2     | [**notificação do VDS \_ Pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_modificação de \_ pacote de NF do VDS \_**                 | 3     | [**notificação do VDS \_ Pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **\_chegada do \_ volume da NF do VDS \_**               | 4     | [**\_notificação de volume do VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **desparte do volume do VDS \_ NF \_ \_**               | 5     | [**\_notificação de volume do VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **\_ \_ Modificar volume do VDS NF \_**               | 6     | [**\_notificação de volume do VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **\_progresso da \_ \_ recriação do \_ volume do VDS NF** | 7     | [**\_notificação de volume do VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **chegada de disco do VDS \_ NF \_ \_**                 | 8     | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **desparte do disco do VDS \_ NF \_ \_**                 | 9     | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **\_modificação de \_ disco de NF do VDS \_**                 | 10    | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partição  | **\_chegada da \_ partição de NF do VDS \_**            | 11    | [**\_notificação de partição VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partição  | **desparte da partição da NF do VDS \_ \_ \_**            | 12    | [**\_notificação de partição VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partição  | **\_modificação da \_ partição da NF do VDS \_**            | 13    | [**\_notificação de partição VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsistema  | **\_chegada do \_ \_ subsistema do VDS NF \_**          | 101   | [**\_notificação de \_ SUBsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsistema  | **\_SUBparte \_ do \_ subsistema VDS NF \_**          | 102   | [**\_notificação de \_ SUBsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsistema  | **\_modificação do \_ \_ subsistema do VDS NF \_**          | 151   | [**\_notificação de \_ SUBsistema VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **\_chegada do \_ controlador de NF do VDS \_**           | 103   | [**notificação do VDS \_ Controller \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **Depart do controlador de NF-VDS \_ \_ \_**           | 104   | [**notificação do VDS \_ Controller \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **\_modificação do \_ controlador de NF do VDS \_**           | 350   | [**notificação do VDS \_ Controller \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **controlador de NF-VDS \_ \_ \_ removido**          | 351   | [**notificação do VDS \_ Controller \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Porta       | **\_modificação da \_ porta de NF do VDS \_**                 | 352   | [**\_notificação de porta VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Porta       | **porta do VDS \_ NF \_ \_ removida**                | 353   | [**\_notificação de porta VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Unidade      | **\_chegada da \_ unidade de NF do VDS \_**                | 105   | [**\_notificação da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidade      | **desparte da unidade da NF de VDS \_ \_ \_**                | 106   | [**\_notificação da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidade      | **\_ \_ Modificar unidade de NF do VDS \_**                | 107   | [**\_notificação da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidade      | **unidade de NF do VDS \_ \_ \_ removida**               | 354   | [**\_notificação da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **\_chegada de \_ LUN de NF-VDS \_**                  | 108   | [**\_notificação de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **canpartção de LUN do VDS \_ NF \_ \_**                  | 109   | [**\_notificação de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **\_modificação de \_ LUN de NF do VDS \_**                  | 110   | [**\_notificação de LUN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

O VDS gera as notificações restantes. A tabela a seguir lista as constantes de notificação baseadas em serviço por categoria.



| Category     | Notificação                                | Valor | Link para a descrição do evento                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disco         | **chegada de disco do VDS \_ NF \_ \_**                   | 8     | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **desparte do disco do VDS \_ NF \_ \_**                   | 9     | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **\_modificação de \_ disco de NF do VDS \_**                   | 10    | [**\_notificação de disco VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Letra da unidade | **letra da unidade de NF do VDS \_ \_ \_ \_ gratuita**            | 201   | [**\_notificação de \_ letra da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Letra da unidade | **\_atribuição de \_ letra da unidade de NF-VDS \_ \_**          | 202   | [**\_notificação de \_ letra da unidade VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Sistema de arquivos  | **\_modificação do \_ sistema de arquivos \_ \_ do VDS NF**           | 203   | [**\_notificação do \_ sistema de arquivos VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Sistema de arquivos  | **\_progresso do \_ formato do sistema de arquivos \_ \_ do VDS NF \_** | 204   | [**\_notificação do \_ sistema de arquivos VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volume       | **\_alteração dos \_ pontos de montagem \_ \_ do VDS NF**          | 205   | [**\_notificação do \_ ponto de montagem do VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink:: onnotificar**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
