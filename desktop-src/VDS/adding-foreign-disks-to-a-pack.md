---
description: Adicionando discos externos a um pacote
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Adicionando discos externos a um pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297505"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Adicionando discos externos a um pacote

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Normalmente, um disco externo é um disco dinâmico que é alocado em um computador e fisicamente movido para outro computador. No entanto, qualquer disco que pertença a um pacote que não seja o pacote online é considerado um disco externo que pertence a um pacote de disco externo.

Um pacote estrangeiro tem o **sinalizador \_ \_ estrangeiro PKF Foreign** definido no membro **ulFlags** da estrutura de [**\_ \_ prop do VDS Pack**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) . Os pacotes estrangeiros estão sempre offline.

O procedimento a seguir descreve como importar um ou mais discos externos.

**Para importar um ou mais discos estrangeiros**

1.  Mova os discos para o novo computador.
2.  No novo computador, use o método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) para instalar os discos externos.
3.  Selecione o pacote online para ser o pacote de destino que recebe os discos externos. Se não existir nenhum pacote online, use o método [**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um novo pacote vazio.
4.  Use o método [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) para importar os discos para o novo pacote dinâmico.
5.  Use o método [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) para enumerar os pacotes e [**IVdsPack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) para determinar qual pacote agora é o pacote online.

Se você criar um novo pacote de destino vazio, os discos externos não serão realmente migrados para esse pacote. Em vez disso, o pacote estrangeiro é marcado como online, o sinalizador **\_ \_ estrangeiro do VDS PKF** para o pacote é limpo (portanto, o pacote não é mais estrangeiro) e o pacote de destino que você criou é Descartado.

> [!Note]  
> Use o método [**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar discos não alocados, discos não reivindicados por um provedor, a um pacote. Um disco não alocado não pode ser estrangeiro.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider:: createpack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
