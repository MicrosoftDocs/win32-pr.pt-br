---
description: Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas de sistema de arquivos na origem e no destino. Essas pastas COMREPL estão todas com raiz na replicação com% systemdir% \\ \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gerenciamento de arquivos (serviços de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500894"
---
# <a name="file-management"></a>Gerenciamento de Arquivos

Para habilitar a transferência de arquivos de aplicativo, o COMREPL gerencia automaticamente conjuntos de pastas de sistema de arquivos na origem e no destino. Essas pastas COMREPL estão todas com raiz na replicação com% systemdir% \\ \\ .

## <a name="source-folders"></a>Pastas de origem



| Pasta                   | Finalidade                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Replicar<br/> | Os aplicativos exportados durante a fase de preparação são armazenados aqui.<br/> Essa pasta é substituída sempre que a fase de preparação é executada em um determinado computador de origem. Essa pasta nunca é excluída explicitamente, portanto, a replicação para destinos pode ocorrer a qualquer momento depois que a origem é preparada.<br/> Cada aplicativo é armazenado em sua própria subpasta denominada <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Pastas de destino



| Pasta                    | Finalidade                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | A fase de cópia copia todos os arquivos e subpastas de Réplicaname na origem para ReplicaNew no destino. Qualquer conteúdo anterior de ReplicaNew é excluído sempre que a fase de cópia é executada em relação a um determinado destino.<br/> Essa pasta só existe enquanto o processo de replicação está em execução. (Consulte ReplicaCurrent.)<br/>           |
| ReplicaCurrent<br/> | Os aplicativos replicados atualmente instalados no destino são armazenados aqui.<br/> Quando a fase de instalação é iniciada, a pasta ReplicaNew é renomeada como ReplicaCurrent. Se houver uma pasta ReplicaCurrent existente, ela será renomeada para ReplicaOld. Se houver uma pasta ReplicaOld existente, seu conteúdo será excluído.<br/> |
| ReplicaOld<br/>     | Salva os arquivos de aplicativo instalados durante o próximo à última replicação. Esses arquivos são salvos somente para fins de backup.<br/>                                                                                                                                                                                                        |



 

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

 

 




