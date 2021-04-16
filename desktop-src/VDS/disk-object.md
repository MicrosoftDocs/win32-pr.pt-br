---
description: Objeto de disco
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Objeto de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551216"
---
# <a name="disk-object"></a>Objeto de disco

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de disco modela um disco físico baseado em host. O provedor de software que está sendo executado no host local pode acessar um LUN como um disco quando o objeto de LUN é desmascarado para o host local. Para obter mais informações sobre o mascaramento de LUN, consulte o [objeto LUN](lun-object.md).

Cada objeto de disco contribui para exatamente um objeto de pacote; no entanto, um disco pode contribuir com extensões para qualquer número de volumes dentro de um pacote. Você pode designar um disco para ser um hot spare.

## <a name="partition-to-volume-mapping"></a>Mapeamento de partição para volume

O sistema operacional inclui suporte para discos básicos e dinâmicos. O VDS fornece um provedor básico e um provedor dinâmico para gerenciar esses tipos de disco. Discos básicos nunca são tolerantes a falhas. Discos dinâmicos podem ser tolerantes a falhas se o sistema operacional permitir essa ligação de volume. Discos básicos e dinâmicos podem conter partições que são estruturadas de acordo com um dos seguintes estilos de partição: MBR (registro mestre de inicialização) ou GPT (tabela de partição GUID). O particionamento MBR tem até quatro partições primárias ou três partições primárias, mais uma partição estendida com unidades lógicas infinitas. O particionamento GPT fornece até 128 partições primárias.

A descrição a seguir é geral por natureza. Ele mostra a relação típica entre partições e volumes, para os quais há várias exceções. Para obter uma descrição detalhada do mapeamento de partição para volume, consulte a interface [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) . O mapeamento de partição para volume varia dependendo do tipo de disco, básico ou dinâmico.

-   Discos básicos

    Uma partição em um disco básico é mapeada diretamente para um volume, na maioria dos casos, e pode ser estilizada como uma partição MBR ou GPT. A ilustração a seguir mostra o mapeamento de ambas as versões de partições MBR. No primeiro caso, as partições (P1 a P4) são mapeadas diretamente para volumes (V1 a V4). Uma ext (partição estendida) substitui P4 no segundo estilo MBR. O número de unidades lógicas dentro da partição estendida que mapeia para volumes é ilimitado.

    ![Mostra duas opções de mapeamento para partições M R.](images/vdsbasicmapping.png)

    As partições GPT (P1 a P128) na próxima ilustração são mapeadas diretamente para volumes (V1 a V128), se todas as partições disponíveis estiverem em uso. Um disco GPT não faz uso de uma partição estendida como uma maneira de melhorar a usabilidade.

    ![Mostra uma partição GPT.](images/vdsbasicmappinggpt.png)

-   Discos dinâmicos

    Um tipo de partição especial em um disco dinâmico é mapeado para um grande número de volumes. Para obter um limite estimado imposto pelo provedor dinâmico, consulte o [objeto Pack](pack-object.md). Como mostra a ilustração a seguir, pode haver qualquer número de extensões dentro do P1 que são mapeadas para volumes.

    ![Mostra um tipo de partição especial em um disco dinâmico.](images/vdsdynamicmapping.png)

Independentemente do tipo de disco, um disco pode conter uma ou mais extensões de disco. Uma extensão de disco é um intervalo contíguo de blocos lógicos expostos pelo disco. Por exemplo, uma extensão de disco pode representar um volume inteiro, uma parte de um volume estendido, um membro de um volume distribuído ou um plex de um volume espelhado.

### <a name="working-with-disks"></a>Trabalhando com discos

Use o método [**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar um disco a um pacote existente. Os chamadores podem obter um ponteiro para um disco específico selecionando o objeto de disco desejado da enumeração que é retornada pelo método [**IVdsPack:: QueryDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) . Da mesma forma, você pode invocar o método [**IVdsDisk:: getpack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) para determinar qual pacote contém um determinado disco.

Você pode mover um disco de um pacote para outro chamando o método [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) . (O VDS não oferece suporte à migração de um disco básico entre pacotes controlados pelo provedor básico.) Você também pode mover um pacote para outro host movendo fisicamente todos os discos do pacote para o novo host. O pacote se move com os discos e aparece como um pacote estrangeiro no novo host. Para obter instruções, consulte [adicionando discos externos a um pacote](adding-foreign-disks-to-a-pack.md).

Além de um identificador de objeto, um nome, um endereço, um tipo de dispositivo e um tipo de mídia, as propriedades de objeto de disco incluem o status do disco, a integridade e os sinalizadores; o tamanho em bytes, bytes por setor, setores por faixa e faixas por cilindro; e o tipo de partição e de barramento.

A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que são sempre expostas por este objeto | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)e [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** Não há suporte para a interface [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) .<br/> **Windows Vista:** A interface [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) não tem suporte até o Windows Vista com Service Pack 1 (SP1); Use [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) em vez disso. Não há suporte para a interface [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) .<br/> **Windows Server 2003:** As interfaces [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)e [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) não têm suporte.<br/> |
| Interfaces que podem ser expostas por este objeto     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Consulte o [objeto LUN](lun-object.md) para interfaces adicionais que são expostas se o disco for um LUN.)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumerações associadas                           | [**VDS \_ \_Sinalizador de disco**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag), [**\_ \_ status do disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_status), [**\_ \_ sinalizador de partição VDS**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag), [**\_ \_ estilo de partição VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)e [**\_ \_ \_ tipo de extensão de disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Estruturas associadas                             | [**VDS \_ \_Prop de disco**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), [**\_ \_ notificação de disco VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**\_ \_ disco de entrada VDS**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**partição VDS \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**informações de partição VDS \_ \_ \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**informações de \_ partição VDS \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)e [**\_ \_ extensão de disco VDS**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de provedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto Pack](pack-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[Adicionando discos externos a um pacote](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

