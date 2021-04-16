---
description: Objeto do controlador
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: Objeto do controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567372"
---
# <a name="controller-object"></a>Objeto do controlador

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de controlador modela um controlador em um subsistema. Os controladores são contidos por subsistemas, e cada controlador tem uma ou mais portas de controlador por meio das quais o computador host pode gravar e ler de LUNs. Um único controlador pode ser definido simultaneamente como ativo para um LUN e inativo para outros. Um controlador que está ativo para um LUN especificado carrega a responsabilidade de lidar com a entrada e a saída do LUN. A figura a seguir ilustra essa ideia.

![Diagrama que mostra um "controlador" com um LUN ativo à esquerda e dois LUNs ativos à direita.](images/vdscontroller.png)

**VDS 1,0:** Cada um dos controladores de um subsistema é definido como ativo ou inativo em relação a cada um dos LUNs das superfícies do subsistema.

Os aplicativos VDS usam o método [**IVdsSubSystem:: QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) para determinar os controladores contidos em um subsistema específico. Os chamadores podem obter um ponteiro para um controlador específico selecionando o objeto do controlador desejado da enumeração que é retornada pelo método **QueryControllers** . Com um objeto de controlador, um chamador pode definir o status do controlador, consultar seus LUNs associados, consultar suas portas do controlador e liberar e invalidar o cache.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto do controlador incluem o status e a integridade do controlador e uma contagem das portas.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| Interfaces que são sempre expostas por este objeto no VDS 1,1 e 2,0 Fibre Channel somente provedores | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| Interfaces que podem ser expostas por este objeto                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| Enumerações associadas                                                                           | [**VDS \_ \_status do controlador**](/windows/desktop/api/Vds/ne-vds-vds_controller_status).                                                                      |
| Estruturas associadas                                                                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) [**\_ \_ Notificação**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)de controlador do VDS e de prop. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
