---
description: Objeto de porta do controlador
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objeto de porta do controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759817"
---
# <a name="controller-port-object"></a>Objeto de porta do controlador

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de porta do controlador modela uma porta do controlador em um subsistema. Os computadores host podem gravar e ler de LUNs por meio de portas do controlador. As portas do controlador são contidas por controladores em um subsistema. No VDS 1,1 e VDS 2.0, cada uma das portas do controlador de um subsistema é definida como ativa ou inativa em relação a cada um dos LUNs que as superfícies do subsistema. Uma única porta do controlador pode ser definida simultaneamente como ativa para um LUN e inativa para outros. Uma porta de controlador que está ativa para um determinado LUN transporta a responsabilidade pelo tratamento de entrada e saída do LUN.

As portas do controlador ativo servem como um dos pontos de extremidade dos caminhos do MPIO em Fibre Channel provedores de hardware, nos quais as políticas de balanceamento de carga podem ser impostas.

Use o método [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) para determinar as portas do controlador que estão contidas em um controlador específico. Os chamadores podem obter um ponteiro para uma porta de controlador específica selecionando o objeto de porta do controlador desejado da enumeração que é retornada pelo método **QueryControllerPorts** . Com um objeto de controlador, um chamador pode definir o status da porta do controlador e a consulta para seus LUNs associados.

As propriedades do objeto do controlador incluem um identificador de objeto, um nome, um número de série e o status da porta do controlador.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                              | Elemento                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto no VDS 1,1 e 2,0 Fibre Channel somente provedores | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Enumerações associadas                                                                           | [**\_status da porta VDS \_**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Estruturas associadas                                                                             | [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) Notificação de porta de porta do [ **VDS \_ \_** e prop](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
