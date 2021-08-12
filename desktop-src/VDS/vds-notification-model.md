---
description: Notificações de VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notificações de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931731cc9c2b4aa73f7599c1fcbfad2f885bc74978ab15ba4e1efbf9d2a7522c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603104"
---
# <a name="vds-notifications"></a>Notificações de VDS

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um provedor pode enviar uma notificação de evento para o VDS, e o VDS pode, por sua vez, encaminhar a notificação para aplicativos. O modelo de notificação usado pelo VDS é semelhante ao modelo de ponto de conexão usado por objetos COM.

O VDS gera notificações de serviço para eventos como uma atribuição de letra de unidade ou a chegada de um disco não alocado. Depois que o VDS aloca um disco a um provedor, o provedor é responsável por gerar as notificações associadas. A ilustração a seguir mostra as interfaces e os métodos usados no modelo de notificação do VDS.

![Diagrama que mostra a interface e os métodos (Advise, OnLoad e OnNotify) entre Aplicativos, Serviço de Disco Virtual e Provedores V D S.](images/vdsnotification.png)

Para receber notificações, o VDS registra sua interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) com o objeto do provedor chamando o método [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) e passando um ponteiro para a interface. Quando ocorre um evento de notificação, como a chegada de um novo volume ou unidade, o provedor passa a estrutura de notificação apropriada para vDS como um parâmetro de método [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

O processo é semelhante entre um aplicativo e o VDS. Especificamente, para receber notificações, um aplicativo registra sua interface [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) com VDS chamando o método [**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) e passando um ponteiro para a interface. Quando o VDS recebe uma notificação de um provedor, ele passa a estrutura de notificação apropriada para aplicativos registrados como um parâmetro de método [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

> [!Note]  
> Um aplicativo que chama [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) eventualmente deve chamar o [**método IVdsService::Unadvise.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) O ideal é que ele **chame Unadvise** assim que não precisar mais receber notificações.

 

A tabela a seguir lista as notificações geradas pelo provedor por tipo de objeto.



| Objeto     | Notificação                              | Valor | Link para a descrição do evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS \_ NF \_ PACK \_ ARRIVE**                 | 1     | [**NOTIFICAÇÃO DO PACOTE VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ PACK \_ DEPART**                 | 2     | [**NOTIFICAÇÃO DO PACOTE VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **MODIFICAÇÃO DO \_ PACOTE NF \_ DO VDS \_**                 | 3     | [**NOTIFICAÇÃO DO PACOTE VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volume     | **VDS \_ NF \_ VOLUME \_ ARRIVE**               | 4     | [**NOTIFICAÇÃO DE VOLUME de VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **SAÍDA DO \_ VOLUME NF do VDS \_ \_**               | 5     | [**NOTIFICAÇÃO DE VOLUME de VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **MODIFICAÇÃO DE \_ VOLUME NF do VDS \_ \_**               | 6     | [**NOTIFICAÇÃO DE VOLUME de VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volume     | **ANDAMENTO DA RECRIAÇÃO \_ DO VOLUME NF do VDS \_ \_ \_** | 7     | [**NOTIFICAÇÃO DE VOLUME de VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **VDS \_ NF \_ DISK \_ ARRIVE**                 | 8     | [**NOTIFICAÇÃO DE DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **VDS \_ NF \_ DISK \_ DEPART**                 | 9     | [**NOTIFICAÇÃO DE DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **MODIFICAÇÃO DE \_ DISCO NF \_ VDS \_**                 | 10    | [**NOTIFICAÇÃO DE DISCO VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partição  | **VDS \_ NF \_ PARTITION \_ ARRIVE**            | 11    | [**NOTIFICAÇÃO DE \_ PARTIÇÃO DE VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partição  | **PARTIÇÃO \_ DO VDS NF \_ \_ DEPART**            | 12    | [**NOTIFICAÇÃO DE \_ PARTIÇÃO DE VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partição  | **MODIFICAÇÃO DA \_ PARTIÇÃO NF \_ VDS \_**            | 13    | [**NOTIFICAÇÃO DE \_ PARTIÇÃO DE VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsistema  | **CHEGADA DO SUBSISTEMA \_ VDS NF \_ \_ \_**          | 101   | [**NOTIFICAÇÃO DO \_ SUBSISTEMA VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsistema  | **SAÍDA DO SUBSISTEMA \_ VDS NF \_ \_ \_**          | 102   | [**NOTIFICAÇÃO DO \_ SUBSISTEMA VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsistema  | **MODIFICAÇÃO DO SUBSISTEMA \_ VDS NF \_ \_ \_**          | 151   | [**NOTIFICAÇÃO DO \_ SUBSISTEMA VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **VDS \_ NF \_ CONTROLLER \_ ARRIVE**           | 103   | [**NOTIFICAÇÃO DO CONTROLADOR \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **SAÍDA DO CONTROLADOR NF do VDS \_ \_ \_**           | 104   | [**NOTIFICAÇÃO DO CONTROLADOR \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **MODIFICAÇÃO DO CONTROLADOR NF do VDS \_ \_ \_**           | 350   | [**NOTIFICAÇÃO DO CONTROLADOR \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **CONTROLADOR \_ VDS NF \_ \_ REMOVIDO**          | 351   | [**notificação do VDS \_ Controller \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
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



| Categoria     | Notificação                                | Valor | Link para a descrição do evento                                                 |
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

 

 
