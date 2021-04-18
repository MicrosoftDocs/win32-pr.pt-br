---
description: O recurso de partições COM+ inclui um cache de partição. Esse cache armazena mapeamentos de usuário para partição e é projetado para evitar o acesso Active Directory repetitivo.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurando o cache de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771496"
---
# <a name="configuring-the-partition-cache"></a>Configurando o cache de partição

O recurso de partições COM+ inclui um cache de partição. Esse cache armazena mapeamentos de usuário para partição e é projetado para evitar o acesso Active Directory repetitivo.

## <a name="changing-cache-size"></a>Alterando o tamanho do cache

O cache de partição consiste em três tabelas, cujo tamanho pode ser modificado para melhorar o desempenho. Essas tabelas consistem no número de entradas de SID no cache, no número de entradas de UO no cache e no número de entradas de partição no cache.

Para alterar esses tamanhos de tabela, os administradores podem modificar os valores de uma chave do registro. A chave do registro e seus valores são os seguintes:

**HKLM \\ software \\ Microsoft \\ com3 \\ PartitionCache**



| Valores da chave                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contém o valor de REG \_ DWORD para o número de entradas de Sid no cache (padrão = 512). Esse valor deve ser definido como um valor maior que o número de identidades exclusivas que um computador servirá na janela de tempo de invalidação de cache.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contém o valor de REG \_ DWORD para o número de entradas de nome de UO no cache (padrão = 64). Esse valor deve ser definido como um valor maior que o número de nomes de UO exclusivos que um computador atenderá na janela de tempo de invalidação de cache.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contém o valor de REG \_ DWORD para o número de entradas de partição no cache (padrão = 1024).<br/> Na janela tempo de invalidação do cache, o valor DWORD deve ser definido como um número maior que o número de partições exclusivas que um computador atenderá. Isso ocorre porque o contexto de um componente pode incluir uma ID de partição para uma partição que não reside nesse computador. <br/> |
| **EntryExpiration**<br/>     | Contém o valor de REG \_ DWORD para a contagem de tiques (cada tique = ~ 7 minutos) até que uma entrada de cache se torne inválida (padrão = 4 (~ 28 minutos)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Liberando o cache

Como o COM+ armazena em cache a partição padrão para os usuários, você talvez queira chamar esse método depois de alterar a partição padrão para um usuário na Active Directory. Os administradores podem fazer isso programaticamente chamando o método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletando métricas de partição](collecting-partition-metrics.md)
</dt> <dt>

[Agrupando aplicativos em partições](grouping-applications-into-partitions.md)
</dt> <dt>

[Gerenciando partições locais](managing-local-partitions.md)
</dt> <dt>

[Gerenciando partições no Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Configurando direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




