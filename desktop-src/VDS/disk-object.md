---
description: Objeto Disk
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Objeto Disk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5979e6e2e25ee6ded15b987ddbcda0c5c135f92452174853577d7781475c5d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137211"
---
# <a name="disk-object"></a>Objeto Disk

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Um objeto de disco modela um disco físico baseado em host. O provedor de software em execução no host local pode acessar um LUN como um disco quando o objeto LUN é não mascarado para o host local. Para obter mais informações sobre o mascaramento de LUN, consulte o [Objeto LUN](lun-object.md).

Cada objeto de disco contribui para exatamente um objeto de pacote; no entanto, um disco pode contribuir com extensão para qualquer número de volumes dentro de um pacote. Você pode designar um disco para ser um sobressalente quente.

## <a name="partition-to-volume-mapping"></a>Mapeamento de partição para volume

O sistema operacional inclui suporte para discos básicos e dinâmicos. O VDS fornece um provedor básico e um provedor dinâmico para gerenciar esses tipos de disco. Os discos básicos nunca são tolerantes a falhas. Os discos dinâmicos poderão ser tolerantes a falhas se o sistema operacional permitir essa associação de volume. Discos básicos e dinâmicos podem conter partições estruturadas de acordo com um dos seguintes estilos de partição: MBR (registro de inicialização mestre) ou GPT (tabela de partição GUID). O particionamento MBR tem até quatro partições primárias ou três partições primárias mais uma partição estendida com unidades lógicas infinitas. O particionamento GPT fornece até 128 partições primárias.

A descrição a seguir é geral por natureza. Ele mostra a relação típica entre partições e volumes, para as quais há várias exceções. Para uma descrição detalhada do mapeamento de partição para volume, consulte a interface [**IVdsAdvancedDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) O mapeamento de partição para volume varia dependendo do tipo de disco, básico ou dinâmico.

-   Discos básicos

    Uma partição em um disco básico é mapeada diretamente para um volume, na maioria dos casos, e pode ser estilada como uma partição MBR ou GPT. A ilustração a seguir mostra o mapeamento para ambas as versões de partições MBR. No primeiro caso, as partições (P1 a P4) mapeiam diretamente para volumes (V1 a V4). Uma partição estendida (Ext) substitui P4 no segundo estilo MBR. O número de unidades lógicas dentro da partição estendida mapeado para volumes é ilimitado.

    ![Mostra duas opções de mapeamento para partições M B R.](images/vdsbasicmapping.png)

    As partições GPT (P1 a P128) na próxima ilustração são mapeando diretamente para volumes (V1 a V128), se todas as partições disponíveis estão em uso. Um disco GPT não usa uma partição estendida como uma maneira de aprimorar a usabilidade.

    ![Mostra uma partição GPT.](images/vdsbasicmappinggpt.png)

-   Discos dinâmicos

    Um tipo de partição especial em um disco dinâmico é mapeado para um grande número de volumes. Para um limite estimado imposto pelo provedor dinâmico, consulte o [objeto pack](pack-object.md). Como mostra a ilustração a seguir, pode haver qualquer número de extensão dentro de P1 que mapeie para volumes.

    ![Mostra um tipo de partição especial em um disco dinâmico.](images/vdsdynamicmapping.png)

Independentemente do tipo de disco, um disco pode conter uma ou mais extensão de disco. Uma extensão de disco é um intervalo contíguo de blocos lógicos expostos pelo disco. Por exemplo, uma extensão de disco pode representar um volume inteiro, uma parte de um volume ampliado, um membro de um volume listado ou um plex de um volume espelhado.

### <a name="working-with-disks"></a>Trabalhando com discos

Use o [**método IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar um disco a um pacote existente. Os chamadores podem obter um ponteiro para um disco específico selecionando o objeto de disco desejado na enumeração retornada pelo [**método IVdsPack::QueryDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) Da mesma forma, você pode invocar o [**método IVdsDisk::GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) para determinar qual pacote contém um determinado disco.

Você pode mover um disco de um pacote para outro chamando o [**método IVdsPack::MigrateDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) (O VDS não dá suporte à migração de um disco básico entre pacotes controlados pelo provedor básico.) Você também pode mover um pacote para outro host movendo fisicamente todos os discos no pacote para o novo host. O pacote se move com os discos e aparece como um pacote externo no novo host. Para obter instruções, [consulte Adicionando discos externos a um pacote](adding-foreign-disks-to-a-pack.md).

Além de um identificador de objeto, um nome, um endereço, um tipo de dispositivo e um tipo de mídia, as propriedades do objeto de disco incluem o status do disco, a saúde e os sinalizadores; o tamanho em bytes, bytes por setor, setores por faixa e faixas por cilindro; e o tipo de barramento e partição.

A tabela a seguir lista interfaces, enumerações e estruturas relacionadas.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que sempre são expostas por este objeto | [**IVdsDisk,**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) [**IVdsDiskOnline,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) [**IVdsAdvancedDisk,**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) [**IVdsAdvancedDisk2,**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2) [**IVdsDiskPartitionMF,**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf) [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)e [**IVdsCreatePartitionEx.**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex) **Windows Server 2008:** Não há suporte para a interface [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)<br/> **Windows Vista:** A interface [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) não tem suporte até Windows Vista com Service Pack 1 (SP1); em vez disso, use [**IVdsDisk2.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) Não há suporte para a interface [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)<br/> **Windows Server 2003:** Não há suporte para as [**interfaces IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskOnline,**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)e [**IVdsDiskPartitionMF2.**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) [](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline)<br/> |
| Interfaces que podem ser expostas por este objeto     | [**IVds Removível.**](/windows/desktop/api/Vds/nn-vds-ivdsremovable) (Consulte [Objeto LUN](lun-object.md) para obter interfaces adicionais que serão expostas se o disco for um LUN.)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumerações associadas                           | [**VDS \_ SINALIZADOR \_ DE DISCO**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag), STATUS DO DISCO [**VDS, \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_status)SINALIZADOR DE PARTIÇÃO [**\_ \_ VDS,**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag)ESTILO DE PARTIÇÃO [**VDS \_ \_**](/windows/win32/api/vds/ne-vds-__vds_partition_style)e [**TIPO DE EXTENSÃO DE DISCO VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Estruturas associadas                             | [**VDS \_ DISK \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop) [**VDS DISK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**VDS INPUT \_ \_ DISK**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**VDS \_ PARTITION \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**VDS \_ PARTITION INFO \_ \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**VDS \_ PARTITION INFO \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)e [**VDS DISK \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do provedor de software](software-provider-objects.md)
</dt> <dt>

[Objeto Pack](pack-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> <dt>

[Adicionando discos externos a um pacote](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

