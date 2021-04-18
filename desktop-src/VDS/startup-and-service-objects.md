---
description: O VDS fornece objetos para executar atividades relacionadas ao serviço. Este tópico descreve cada objeto.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Inicialização e objetos de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785391"
---
# <a name="startup-and-service-objects"></a>Inicialização e objetos de serviço

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O VDS fornece objetos para executar atividades relacionadas ao serviço. Este tópico descreve cada objeto.

## <a name="service-loader-object"></a>Objeto do carregador de serviço

O objeto do carregador de serviço fornece os métodos que são usados por aplicativos para carregar e inicializar o VDS. Para preparar o VDS para uso, um aplicativo deve executar as seguintes operações:

-   Crie uma instância do objeto do carregador de serviço, que retorna a interface [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) .
-   Chame o método [**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para carregar o serviço.

Para obter um exemplo de código, consulte [carregando o VDS](loading-vds.md).

Sempre permita que o serviço seja inicializado completamente antes de chamar os métodos expostos pelo objeto de serviço. Use o método [**IVdsService:: IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) para determinar o status do processo de carregamento. Use o método [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para bloquear chamadas para objetos VDS até que a inicialização seja concluída.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Enumerações associadas                           | Nenhum.                                           |
| Estruturas associadas                             | Nenhum.                                           |



 

## <a name="service-object"></a>Objeto de serviço

O objeto de serviço é um objeto multifuncional que é central para todos os aplicativos VDS. Com esse objeto, um chamador pode executar as seguintes operações:

-   Determine o status da inicialização do serviço.
-   Recupere todos os provedores de hardware ou software registrados com VDS.
-   Relatório em discos não alocados.
-   Retornar o tipo de sistema de arquivos e a letra da unidade associada aos volumes em um disco.
-   Remova os caminhos do modo de usuário não utilizados e as pastas montadas do registro e atualize os discos.
-   Receber notificações do VDS.
-   Reinicialize o host.
-   Recupere Fibre Channel portas HBA ou adaptadores de iniciador iSCSI no computador local.
-   Prepare com segurança LUNs expostos como discos no computador local para remoção.

As estruturas de notificação do VDS passam GUIDs de objeto para todos os aplicativos registrados com o VDS para receber notificações. Use o método [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para converter um GUID de objeto em um ponteiro de objeto. Para obter uma descrição mais completa do modelo de notificação, consulte [notificações do VDS](vds-notification-model.md).

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfaces que são sempre implementadas, mas não expostas a aplicativos | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumerações associadas                                                | [**VDS \_ \_ \_ sinalizador do provedor de consultas**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**\_ \_ tipo de objeto VDS**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**\_ \_ sinalizador do serviço VDS**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**\_ \_ \_ sinalizador de letra da unidade VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**\_ \_ \_ sinalizador do sistema de arquivos VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), [**\_ \_ \_ \_ sinalizador de prop do sistema de arquivos VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Estruturas associadas                                                  | [**VDS \_ \_prop do serviço**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**\_ \_ \_ prop do sistema de arquivos VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), tipo de sistema de [**\_ arquivos VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), notificação de [**\_ letra da unidade \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), notificação do [**\_ \_ sistema \_ de arquivos VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**notificação do ponto de montagem do VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** não há suporte para essas interfaces até o Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Objeto de adaptador do iniciador

Um objeto de adaptador de iniciador modela um adaptador de iniciador iSCSI no computador host do serviço VDS. O serviço VDS só pode exibir os adaptadores iniciadores no computador local. A função de um objeto de adaptador do iniciador é para o gerenciamento de sessões de logon do computador local para destinos iSCSI.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Enumerações associadas                           | [**VDS \_ \_ \_ tipo de logon iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ \_ \_ sinalizador de logon iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**\_ \_ \_ tipo de autenticação VDS iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Estruturas associadas                             | [**VDS \_ \_prop do \_ adaptador \_ do iniciador iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003:** esta interface não tem suporte até o Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Objeto do portal do iniciador

Um objeto do portal do iniciador modela um portal do iniciador iSCSI em um iniciador iSCSI. Um portal do iniciador é a combinação de um endereço IP e uma porta por meio da qual um computador host se conecta a um portal em um subsistema iSCSI. A função de um objeto do portal do iniciador é servir como um dos pontos de extremidade de um caminho do MPIO e definir as configurações de segurança do IPSEC.

A tabela a seguir lista as interfaces, enumerações e estruturas relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Enumerações associadas                           | [**VDS \_ \_ \_ sinalizador de IPSec iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Estruturas associadas                             | [**VDS \_ \_portal do iniciador iSCSI \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**\_ \_ \_ chave IPsec do VDS iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**\_ IPAddress do VDS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** esta interface não tem suporte até o Windows Server 2003 R2.

## <a name="hba-port-object"></a>Objeto porta HBA

O objeto de porta HBA modela um Fibre Channel porta de HBA (adaptador de barramento de host).

Use o método [**IVdsServiceHba:: QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) para determinar as portas do HBA que são conhecidas pelo VDS no computador local.

A tabela a seguir lista as interfaces, enumerações e estruturas relacionadas.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Enumerações associadas                           | [**VDS \_ \_tipo hbaport**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**\_ \_ status do VDS hbaport**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**sinalizador de velocidade do VDS \_ hbaport \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Estruturas associadas                             | [**VDS \_ \_prop hbaport**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** esta interface não tem suporte até o Windows Server 2003 R2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Carregando VDS](loading-vds.md)
</dt> <dt>

[**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notificações do VDS](vds-notification-model.md)
</dt> </dl>

 

 
