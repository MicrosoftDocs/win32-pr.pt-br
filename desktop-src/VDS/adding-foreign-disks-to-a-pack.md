---
description: Adicionando discos externos a um pacote
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Adicionando discos externos a um pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755451"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Adicionando discos externos a um pacote

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Normalmente, um disco externo é um disco dinâmico alocado em um computador e movido fisicamente para outro computador. No entanto, qualquer disco que pertence a um pacote diferente do pacote online é considerado um disco externo que pertence a um pacote de discos externos.

Um pacote externo tem o **sinalizador \_ FOREIGN PKF \_ VDS** definido no membro **ulFlags** da estrutura [**PROP do VDS \_ PACK. \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) Os pacotes externos estão sempre offline.

O procedimento a seguir descreve como importar um ou mais discos externos.

**Para importar um ou mais discos externos**

1.  Mova os discos para o novo computador.
2.  No novo computador, use o [**método IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) para instalar os discos externos.
3.  Selecione o pacote online para ser o pacote de destino que recebe os discos externos. Se não houver nenhum pacote online, use o [**método IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) para criar um novo pacote vazio.
4.  Use o [**método IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) para importar os discos para o novo pacote dinâmico.
5.  Use o método [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) para enumerar os pacotes e [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) para determinar qual pacote agora é o pacote online.

Se você criar um novo pacote de destino vazio, os discos externos não serão realmente migrados para esse pacote. Em vez disso, o pacote externo é marcado online, o sinalizador FOREIGN do **\_ PKF \_ VDS** para o pacote é limpo (portanto, o pacote não é mais externo) e o pacote de destino que você criou é descartado.

> [!Note]  
> Use o [**método IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) para adicionar discos não alocados – discos não reivindicados por um provedor – a um pacote. Um disco não alocado não pode ser externo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
