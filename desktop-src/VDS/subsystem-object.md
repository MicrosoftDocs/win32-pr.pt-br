---
description: Objeto subsistema
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: Objeto subsistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af9837da90497b07d133362c0a61549a63665f2c75d4c97b2d07369e4589fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603141"
---
# <a name="subsystem-object"></a>Objeto subsistema

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de subsistema modela um subsistema de armazenamento. Um subsistema é um compartimento RAID ou uma placa RAID PCI. Um único computador host pode ser conectado a qualquer número de subsistemas. Cada subsistema é gerenciado por exatamente um provedor de hardware. Em uma configuração san, a classe de subsistema representa um compartimento de armazenamento SAN.

Um subsistema pode conter qualquer número de controladores e unidades e pode aparecer (sem máscara) qualquer número de LUNs para o computador no qual o provedor de hardware está em execução. Subsistemas de extremidade superior podem desacodar LUNs para outros computadores na rede. Cada unidade de disco dentro de um subsistema é conectada a um barramento e ocupa um slot no barramento. Cada controlador dentro de um subsistema tem uma ou mais portas de controlador.

A ilustração a seguir mostra os dispositivos físicos contidos em um subsistema (LUNs não são mostrados) e as relações entre eles.

![Diagrama que mostra um subsistema começando com 'Portas' à esquerda, movendo para 'Controladores' e, em seguida, um 'Barramento' com 'Slots' levando a 'Unidades' individuais.](images/vdssubsystem.png)

Os aplicativos VDS usam o método [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) para consultar os subsistemas que pertencem a um provedor de hardware específico. Os chamadores podem obter um ponteiro para um subsistema específico selecionando o objeto de subsistema desejado na enumeração retornada pelo **método QuerySubSystems.** Com um objeto de subsistema, você pode definir o status do subsistema, criar LUNs, substituir unidades e consultar controladores, unidades e LUNs.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto de subsistema incluem o status do subsistema, a saúde e os sinalizadores; uma contagem dos controladores, slots e caminhões; e uma configuração de prioridade de recomposição.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas.



| Tipo                                                                                      | Elemento                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto                                         | [**IVdsSubSystem.**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)                                                                                          |
| Interfaces que sempre são expostas por esse objeto somente em provedores iSCSI VDS 1.1 e 2.0 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) [**e IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).             |
| Interfaces que podem ser expostas por este objeto                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) [**e IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).                               |
| Enumerações associadas                                                                   | [**VDS \_ \_ \_ SUB-SINALIZADOR DE SISTEMA**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) E STATUS DO [**\_ \_ SUBSISTEMA \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).             |
| Estruturas associadas                                                                     | [**VDS \_ SUB \_ SYSTEM \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) e [**VDS \_ SUB SYSTEM \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification). |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
