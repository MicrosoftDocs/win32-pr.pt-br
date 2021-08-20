---
description: O VDS fornece objetos para executar atividades relacionadas ao serviço. Este tópico descreve cada objeto.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Objetos de inicialização e serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a87c7e52a263d03e80f44911f72db5f49259baf33a7b2f90680f30bb3b2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125926"
---
# <a name="startup-and-service-objects"></a>Objetos de inicialização e serviço

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O VDS fornece objetos para executar atividades relacionadas ao serviço. Este tópico descreve cada objeto.

## <a name="service-loader-object"></a>Objeto Service Loader

O objeto do carregador de serviço fornece os métodos usados pelos aplicativos para carregar e inicializar o VDS. Para preparar o VDS para uso, um aplicativo deve executar as seguintes operações:

-   Crie uma instância do objeto do carregador de serviço, que retorna a interface [**IVdsServiceLoader.**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)
-   Chame o [**método IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para carregar o serviço.

Para ver um exemplo de código, [consulte Carregando VDS](loading-vds.md).

Sempre permita que o serviço seja inicializado completamente antes de chamar os métodos expostos pelo objeto de serviço. Use o [**método IVdsService::IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) para determinar o status do processo de carregamento. Use o [**método IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para bloquear chamadas para objetos VDS até que a inicialização seja concluída.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsServiceLoader.**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) |
| Enumerações associadas                           | Nenhum.                                           |
| Estruturas associadas                             | Nenhum.                                           |



 

## <a name="service-object"></a>Objeto service

O objeto de serviço é um objeto multifuncional que é central para todos os aplicativos VDS. Com esse objeto, um chamador pode executar as seguintes operações:

-   Determine o status da inicialização do serviço.
-   Recupere todos os provedores de hardware ou software registrados no VDS.
-   Relatório sobre discos não alocados.
-   Retornar o tipo de sistema de arquivos e a letra da unidade associadas aos volumes em um disco.
-   Remova caminhos de modo de usuário não utilizado e pastas montadas do registro e atualize os discos.
-   Receber notificações de VDS.
-   Reinicialize o host.
-   Recupere Fibre Channel portas HBA ou adaptadores de iniciador iSCSI no computador local.
-   Prepare luns expostos com segurança como discos no computador local para remoção.

As estruturas de notificação de VDS passam GUIDs de objeto para todos os aplicativos registrados no VDS para receber notificações. Use o [**método IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para converter um GUID de objeto em um ponteiro de objeto. Para obter uma descrição mais completa do modelo de notificação, consulte [Notificações de VDS](vds-notification-model.md).

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto                      | [**IVdsService,**](/windows/desktop/api/Vds/nn-vds-ivdsservice) [**IVdsServiceHba,**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* [**IVdsServiceIscsi,**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfaces que são sempre implementadas, mas não expostas a aplicativos | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumerações associadas                                                | [**VDS \_ SINALIZADOR DO \_ PROVEDOR \_ DE**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)CONSULTAS , TIPO DE OBJETO [**VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_object_type), SINALIZADOR DE SERVIÇO [**VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), SINALIZADOR DE LETRA DA UNIDADE [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), SINALIZADOR DO SISTEMA DE ARQUIVOS [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), SINALIZADOR PROP DO SISTEMA DE ARQUIVOS [**VDS \_ \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Estruturas associadas                                                  | [**VDS \_ SERVICE \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**VDS FILE SYSTEM \_ \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**VDS FILE SYSTEM TYPE \_ \_ \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), [**VDS \_ DRIVE LETTER \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), [**VDS \_ FILE SYSTEM \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**VDS \_ MOUNT POINT \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** essas interfaces não têm suporte até Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Objeto do adaptador do iniciador

Um objeto do adaptador do iniciador modela um adaptador do iniciador iSCSI no computador host do serviço VDS. O serviço VDS só pode exibir adaptadores iniciadores no computador local. A função de um objeto de adaptador iniciador é para gerenciar sessões de logon do computador local para destinos iSCSI.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsIscsiInitiatorAdapter.**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \*                                                                                                        |
| Enumerações associadas                           | [**VDS \_ TIPO DE \_ \_ LOGON ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ SINALIZADOR DE \_ LOGON \_ ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), TIPO DE [**\_ AUTH ISCSI \_ \_ DO VDS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Estruturas associadas                             | [**VDS \_ PROP DO ADAPTADOR \_ DO \_ INICIADOR \_ ISCSI.**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop)                                                                                        |



 

**\* Windows Server 2003:** essa interface não tem suporte até Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Objeto do Portal do Iniciador

Um objeto do portal do iniciador modela um portal do iniciador iSCSI em um iniciador iSCSI. Um portal do iniciador é a combinação de um endereço IP e porta por meio do qual um computador host se conecta a um portal em um subsistema iSCSI. A função de um objeto do portal do iniciador é servir como um dos pontos de extremidade de um caminho MPIO e definir as configurações de segurança do IPSEC.

A tabela a seguir lista as interfaces, enumerações e estruturas relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsIscsiInitiatorPortal.**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \*                                                                                                                 |
| Enumerações associadas                           | [**VDS \_ SINALIZADOR ISCSI \_ IPSEC \_**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Estruturas associadas                             | [**VDS \_ ISCSI \_ INITIATOR \_ PORTAL \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS \_ ISCSI \_ IPSEC \_ KEY**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** essa interface não tem suporte até Windows Server 2003 R2.

## <a name="hba-port-object"></a>Objeto de porta HBA

O objeto de porta HBA modela uma Fibre Channel HBA (adaptador de barramento de host).

Use o [**método IVdsServiceHba::QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) para determinar as portas HBA conhecidas pelo VDS no computador local.

A tabela a seguir lista as interfaces, enumerações e estruturas relacionadas.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsHbaPort.**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \*                                                                                                                            |
| Enumerações associadas                           | [**VDS \_ HBAPORT \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS \_ HBAPORT \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS \_ HBAPORT \_ SPEED \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Estruturas associadas                             | [**VDS \_ HBAPORT \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** essa interface não tem suporte até Windows Server 2003 R2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Carregando VDS](loading-vds.md)
</dt> <dt>

[**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notificações de VDS](vds-notification-model.md)
</dt> </dl>

 

 
