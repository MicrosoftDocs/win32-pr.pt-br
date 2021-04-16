---
description: Objeto LUN
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: Objeto LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad74fa65802adb1439360fb2fcdb423c642ef736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779582"
---
# <a name="lun-object"></a>Objeto LUN

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de LUN (número de unidade lógica) modela uma unidade lógica de espaço de armazenamento endereçável que é criada por um provedor de hardware e na superfície de um subsistema. Cada LUN compreende pelo menos um plex de LUN, que é, por sua vez, composto de extensões de uma ou mais unidades.

## <a name="lun-types"></a>Tipos de LUN

O VDS dá suporte a cinco tipos de LUN: simples, estendido, distribuído, espelhado e distribuído com paridade. LUNs simples, estendidos e distribuídos são não tolerantes a falhas; os LUNs espelhados e de paridade são tolerantes a falhas. O restante desta seção descreve cada um dos tipos de LUN VDS.

-   Um LUN simples é um LUN tolerante a falhas que é composto por uma única extensão de unidade contígua de uma única unidade. A extensão contígua pode consistir em um único intervalo de blocos ou vários intervalos de blocos vinculados.
-   Um LUN estendido é um LUN tolerante a falhas que é composto por várias extensões não contíguas de várias unidades. Os dados são gravados linearmente em cada uma das extensões na primeira unidade até que todas as extensões da primeira unidade sejam preenchidas e, em seguida, em cada uma das extensões na segunda unidade, e assim por diante. Os LUNs estendidos oferecem um uso eficiente do espaço da unidade em subsistemas que compõem unidades de vários tamanhos.
-   Um LUN distribuído é um LUN tolerante a falhas que é composto por várias extensões intercaladas e contíguas de várias unidades. LUNs distribuídos usam uma configuração de RAID-0, de modo que os dados são "distribuídos" cíclicamente entre as extensões nas unidades de contribuição. Os LUNs distribuídos funcionam melhor com unidades do mesmo tamanho, modelo e fabricante.
-   LUNs espelhados são LUNs tolerantes a falhas que fornecem a recuperação de desastres duplicando os dados para vários plexes de LUN. Cada plex em um LUN espelhado contém uma cópia dos dados armazenados no Plex original. Cada um dos plexes reside em uma unidade separada. Todos os dados gravados em um LUN espelhado são gravados simultaneamente em cada um de seus plexes. Se uma das unidades contribuintes falhar, o Plex nessa unidade se tornará indisponível, mas o sistema continuará a operar usando o Plex ou os plexes não afetados. Um LUN espelhado pode ter qualquer número de plexes.
-   Distribuídos com LUNs de paridade são LUNs tolerantes a falhas que fornecem recuperação de desastres distribuindo dados de paridade intermitentemente em três ou mais unidades. Se uma das unidades contribuintes falhar, os dados perdidos poderão ser recriados a partir dos dados e da paridade restantes.

## <a name="lun-creation"></a>Criação de LUN

O VDS dá suporte a quatro modelos pelos quais os aplicativos podem criar LUNs: explicitamente direcionados, parcialmente direcionados, automagic e específicos do fornecedor. Todos os provedores de hardware devem dar suporte à criação de LUN explícita e parcialmente direcionada e são altamente incentivados a dar suporte à criação de LUN automagic. (A criação de LUN específica do fornecedor está fora do escopo deste guia.)

A criação de LUN direcionada explicitamente permite que o chamador especifique todos os atributos do LUN. A criação de LUN parcialmente direcionada permite que o chamador especifique somente os atributos que são de interesse específico e, em seguida, permite que o provedor escolha o restante. A criação de LUN automagic envolve habilitar o chamador a simplesmente especificar o tipo de LUN e o tamanho, juntamente com um conjunto de "dicas automágicas" (preferências predefinidas para atributos de LUN) e, em seguida, permitir que o provedor crie o LUN automaticamente.

## <a name="lun-masking"></a>Máscara de LUN

O VDS dá suporte à remoção de máscara de LUN para subsistemas que oferecem esse recurso. Todos os LUNs são exibidos no computador no qual o provedor está em execução. O desmascaramento de LUN permite que um chamador "desmascarar" os LUNs selecionados para outros computadores na rede. Se você remover a máscara de um LUN para um computador, o computador terá acesso ao LUN. Os computadores para os quais um LUN é mascarado não têm.

Um LUN sem máscara expõe as interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) ao host local. Você pode usar o **IVdsDisk** para adicionar um LUN a um pacote de provedor de software, criar e remover volumes, atribuir letras de unidade e assim por diante. Para obter mais informações sobre as operações executadas em um disco, consulte o [objeto Disk](disk-object.md).

Depois que um LUN é remascarado para um computador de destino ou mascarado de um computador de destino, a visibilidade do LUN nesse computador pode não ser alterada até que um novo exame de barramento seja executado. O aplicativo VDS na máquina de destino inicia o novo exame do barramento chamando [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). O início do novo exame de barramento é a responsabilidade do aplicativo VDS, não do provedor de hardware.

## <a name="lun-multipathing"></a>Vários caminhos de LUN

Os provedores de hardware que dão suporte a MPIO (Multipath I/O) podem definir políticas de balanceamento de carga em caminhos entre um LUN e o host local. LUNs que oferecem suporte a esse recurso expõem a interface [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) para o host local.

## <a name="working-with-luns"></a>Trabalhando com LUNs

Use o método [**IVdsSubSystem:: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) para criar um novo objeto LUN. Você pode consultar os LUNs que são exibidos por um subsistema específico invocando o método [**QueryLuns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) , também exposto por [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem). Um chamador pode obter um ponteiro para um LUN específico selecionando o objeto de LUN desejado da enumeração que é retornada por **QueryLuns**. Com um objeto LUN, você pode definir o status do LUN; consultar todos os controladores ativos, plexes e dicas do automagic; estender e reduzir o LUN; Adicionar e remover plexes; definir máscaras; aplicar dicas; e exclua o LUN.

Além de um identificador de objeto, um nome e um número de série, as propriedades do objeto LUN incluem o tipo de LUN, o tamanho, o status, a integridade, o estado de transição e os sinalizadores; uma lista de remoção de máscara; e uma configuração de prioridade de recriação.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Interfaces que são sempre expostas por este objeto no VDS 1,1 e 2,0 Fibre Channel somente provedores | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfaces que são sempre expostas por este objeto somente nos provedores de iSCSI VDS 1,1 e 2,0         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfaces que podem ser expostas por este objeto\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)e [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**windows Server 2008, Windows Vista e Windows Server 2003:** não há suporte para a interface [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) .<br/> |
| Enumerações associadas                                                                           | [**VDS \_ \_Sinalizador de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) e [**\_ \_ status de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)e [**\_ \_ tipo de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Estruturas associadas                                                                             | [**VDS \_ \_Informações de LUN**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information), o [**VDS \_ LUN \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)e a [**\_ \_ notificação de LUN VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Consulte [objeto de disco](disk-object.md) para interface adicional ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) que é exposto se o LUN estiver sem máscara como um disco no computador host local.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto Pack](pack-object.md)
</dt> <dt>

[Objeto de disco](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Adicionando uma letra de unidade a um LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

