---
description: O objeto de provedor modela o programa responsável pelo gerenciamento de armazenamento.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Objeto de provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb64d879b8213970edd5887c2d7a217c434ec38a113d2c9f36cd9e1d73e564d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999457"
---
# <a name="provider-object"></a>Objeto de provedor

\[a partir do Windows 8 e Windows Server 2012, a interface COM do [serviço de disco Virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de Armazenamento Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O objeto de provedor modela o programa responsável pelo gerenciamento de armazenamento. Este objeto fornece acesso ao provedor de software e à funcionalidade do provedor de hardware. Os programas de provedor executam operações em dispositivos de software (volumes e discos) e dispositivos de hardware (subsistemas de armazenamento e matrizes de unidades por trás de controladores RAID).

o VDS registra um objeto de provedor como um objeto COM no registro de Windows e usa interfaces contidas (não agregação) para implementar os objetos restantes, encapsulando todas as interfaces e métodos e adicionando condicionalmente a funcionalidade. Os objetos e as interfaces que são encapsuladas pelo objeto do provedor diferem dependendo do tipo de provedor.

Você não pode criar uma instância de um objeto de provedor diretamente do seu aplicativo. Em vez disso, você deve iniciar o VDS, obter um ponteiro para um objeto de serviço e usar o objeto de serviço para consultar os provedores conhecidos do host. Para obter instruções sobre como carregar o VDS, consulte [Startup and Service Objects](startup-and-service-objects.md).

Use o método [**IVdsService:: QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) para enumerar os programas de provedor registrados em um host. O primeiro parâmetro do método permite que você especifique somente provedores de software, provedores de hardware ou ambos. Com um objeto de provedor, você pode executar operações nos objetos gerenciados por esse provedor. Como mostra a ilustração a seguir, você pode usar os métodos expostos pela interface [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) para criar e consultar objetos de pacote associados a provedores de software. Da mesma forma, você pode usar os métodos na interface [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) para interagir com os objetos do subsistema associados aos provedores de hardware.

![Diagrama que mostra uma ramificação de ' aplicativo ' em ' Providers ', ' Pack ' ou ' subsistema ' e ' eixos '.](images/vdsproviderobject.png)

As propriedades do objeto incluem um identificador de objeto GUID persistente que representa um provedor específico e um segundo GUID que representa a versão do provedor. Observe que outros identificadores de objeto no modelo de objeto do VDS são não persistentes. As propriedades restantes desse objeto incluem um nome de provedor, informações de versão adicionais, o software de tipo de provedor ou hardware), vários sinalizadores e uma configuração de recriação de prioridade que se aplica somente a provedores de software.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas 

| Tipo                                                                                         | Elemento                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfaces que são sempre expostas somente por provedores de software                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfaces que são sempre expostas somente por provedores de hardware                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfaces que podem ser expostas por este objeto                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfaces que podem ser expostas somente por provedores de hardware                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows server 2008, Windows Vista e Windows Server 2003:** não há suporte para a interface [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) .<br/> |
| Interfaces que são sempre implementadas, mas não expostas a aplicativos                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfaces que são sempre implementadas por provedores de hardware, mas não são expostas a aplicativos | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfaces que podem ser implementadas por provedores de hardware, mas não expostas a aplicativos     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Enumerações associadas                                                                      | [**VDS \_ \_Sinalizador do provedor**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**\_ \_ \_ sinalizador do provedor de consultas VDS**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)e [**\_ \_ tipo de provedor VDS**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Estruturas associadas                                                                        | Nenhum.                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[Inicialização e objetos de serviço](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

