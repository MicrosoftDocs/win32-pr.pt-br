---
description: Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas do sistema de arquivos na origem e no destino. Essas pastas COMREPL estão todas enraizada na replicação %systemdir% \\ \\ com.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gerenciamento de Arquivos (Serviços de Componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685287e783dc5ae45d564897a37733568cc150d9af43322d5f435100e8f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307302"
---
# <a name="file-management"></a>Gerenciamento de Arquivos

Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas do sistema de arquivos na origem e no destino. Essas pastas COMREPL estão todas enraizada na replicação %systemdir% \\ \\ com.

## <a name="source-folders"></a>Pastas de origem



| Pasta                   | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Os aplicativos exportados durante a fase de preparação são armazenados aqui.<br/> Essa pasta é substituída sempre que a fase de preparação é executada em um determinado computador de origem. Essa pasta nunca é excluída explicitamente, portanto, a replicação para destinos pode ocorrer a qualquer momento depois que a origem é preparada.<br/> Cada aplicativo é armazenado em sua própria subpasta chamada <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Pastas de destino



| Pasta                    | Finalidade                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | A fase de cópia copia todos os arquivos e subpastas de ReplicaSource na origem para ReplicaNew no destino. Qualquer conteúdo anterior de ReplicaNew é excluído sempre que a fase de cópia é executado em relação a um determinado destino.<br/> Essa pasta existe somente enquanto o processo de replicação está em execução. (Consulte ReplicaCurrent.)<br/>           |
| ReplicaCurrent<br/> | Os aplicativos replicados atualmente instalados no destino são armazenados aqui.<br/> Quando a fase de instalação é iniciada, a pasta ReplicaNew é renomeada para ReplicaCurrent. Se houver uma pasta ReplicaCurrent existente, ela será renomeada como ReplicaOld. Se houver uma pasta ReplicaOld existente, seu conteúdo será excluído.<br/> |
| ReplicaOld<br/>     | Salva os arquivos de aplicativo instalados durante a próxima a última replicação. Esses arquivos são salvos apenas para fins de backup.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro em log e relatório de erros](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicação](replication-phases.md)
</dt> <dt>

[Usando COMREPL](using-comrepl.md)
</dt> <dt>

[O que é replicado](what-gets-replicated.md)
</dt> </dl>

 

 




