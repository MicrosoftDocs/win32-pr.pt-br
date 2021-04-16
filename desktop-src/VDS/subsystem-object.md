---
description: Objeto de subsistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Objeto de subsistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550310"
---
# <a name="subsystem-object"></a>Objeto de subsistema

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de subsistema modela um subsistema de armazenamento. Um subsistema é um compartimento RAID ou uma placa PCI RAID. Um único computador host pode ser conectado a qualquer número de subsistemas. Cada subsistema é gerenciado por exatamente um provedor de hardware. Em uma configuração de SAN, a classe de subsistema representa um compartimento de armazenamento de SAN.

Um subsistema pode conter qualquer número de controladores e unidades e pode trazer a superfície (remover máscara) de qualquer número de LUNs para o computador no qual o provedor de hardware está em execução. Subsistemas de extremidade superior podem remover a máscara de LUNs para outros computadores na rede. Cada unidade de disco em um subsistema está conectada a um barramento e ocupa um slot no barramento. Cada controlador em um subsistema tem uma ou mais portas do controlador.

A ilustração a seguir mostra os dispositivos físicos contidos em um subsistema (LUNs não são mostrados) e as relações entre eles.

![Diagrama que mostra um subsistema começando com ' portas ' à esquerda, movendo para ' controladores ' e, em seguida, um ' barramento ' com ' Slots ' que levam a ' unidades ' individuais.](images/vdssubsystem.png)

Os aplicativos VDS usam o método [**IVdsHwProvider:: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar os subsistemas que pertencem a um provedor de hardware específico. Os chamadores podem obter um ponteiro para um subsistema específico selecionando o objeto subsistema desejado da enumeração que é retornada pelo método **QuerySubSystems** . Com um objeto de subsistema, você pode definir o status do subsistema, criar LUNs, substituir unidades e consultar controladores, unidades e LUNs.

Além de um identificador de objeto, um nome e um número de série, as propriedades de objeto do subsistema incluem o status, a integridade e os sinalizadores do subsistema; uma contagem de controladores, slots e barramentos; e uma configuração de prioridade de recriação.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).                                                                                          |
| Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) e [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfaces que podem ser expostas por este objeto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) e [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumerações associadas                                                                   | [**VDS \_ \_ \_ Sinalizador de subsistema**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) e [**\_ \_ \_ status de subsistema VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Estruturas associadas                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) [**\_ \_ \_ Notificação de subsistema**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification)e de prop-Subsystem de subsistema. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
