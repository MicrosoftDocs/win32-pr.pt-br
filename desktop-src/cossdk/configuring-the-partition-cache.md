---
description: O recurso de partições COM+ inclui um cache de partição. Esse cache armazena mapeamentos de usuário para partição e foi projetado para evitar o acesso repetitivo do Active Directory.
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: Configurando o cache de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906e36065244ab7f2ffa54cad5a7aca33a0c152744af2b6017edb95a8a960b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128958"
---
# <a name="configuring-the-partition-cache"></a>Configurando o cache de partição

O recurso de partições COM+ inclui um cache de partição. Esse cache armazena mapeamentos de usuário para partição e foi projetado para evitar o acesso repetitivo do Active Directory.

## <a name="changing-cache-size"></a>Alterando o tamanho do cache

O cache de partição consiste em três tabelas, cujo tamanho pode ser modificado para melhorar o desempenho. Essas tabelas consistem no número de entradas SID no cache, no número de entradas de UO no cache e no número de entradas de partição no cache.

Para alterar esses tamanhos de tabela, os administradores podem modificar os valores de uma chave do Registro. A chave do Registro e seus valores são os seguinte:

**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**



| Valores da chave                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | Contém o valor \_ REG DWORD para o número de entradas SID no cache (default=512). Esse valor deve ser definido como um valor maior que o número de identidades exclusivas que um computador estará atendendo na janela de tempo de invalidação do cache.<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | Contém o valor REG DWORD para o número de entradas de nome \_ de UO no cache (default=64). Esse valor deve ser definido como um valor maior que o número de nomes de UO exclusivos que um computador estará atendendo na janela de tempo de invalidação do cache.<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | Contém o valor \_ REG DWORD para o número de entradas de partição no cache (default=1024).<br/> Na janela de tempo de invalidação do cache, o valor DWORD deve ser definido como um número maior que o número de partições exclusivas que um computador estará atendendo. Isso acontece porque o contexto de um componente pode incluir uma ID de partição para uma partição que não reside nesse computador. <br/> |
| **EntryExpiration**<br/>     | Contém o valor REG DWORD para a contagem de tiques (cada tique = ~7 minutos) até que uma entrada de cache se torne inválida \_ (default=4 (~28 minutos)).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>Liberando o cache

Como o COM+ armazena em cache a partição padrão para usuários, talvez você queira chamar esse método depois de alterar a partição padrão para um usuário no Active Directory. Os administradores podem fazer isso programaticamente chamando o [**método FlushPartitionCache.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache)

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

[Definindo direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




