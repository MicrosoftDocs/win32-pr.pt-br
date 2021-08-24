---
description: Usando COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Usando COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501cca8d32383e23fc636669e32a80cfdfe96dd658717e41c1618244fc5af81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853876"
---
# <a name="using-comrepl"></a>Usando COMREPL

Para iniciar o utilitário de linha de comando COMREPL, use as seguintes etapas:

1.  Adicione% windir% \\ System32 \\ com ao caminho do ambiente padrão digitando o seguinte no prompt de comando:

    **Definir caminho =% PATH%;% WINDIR% \\ System32 \\ com**

2.  Insira o seguinte comando COMREPL:

    **COMREPL** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**

    em que:

    -   *sourceComputer* é o nome do computador da origem

    -   *targetComputerList* são os nomes de computador dos destinos separados por espaços

    -   **/n** suprime o prompt de confirmação antes de iniciar a replicação

    -   **/v** ecoa a saída do arquivo de log para o console

## <a name="notes"></a>Observações

-   Como o COM+ não é replicado (somente aplicativos e dados de configuração), todos os computadores de destino já devem ter o COM+ instalado.
-   O usuário deve passar as verificações de função para o aplicativo do sistema nos computadores de origem e de destino.
-   Nenhuma conta de computador local que possa ser usada por funções é replicada.
-   O (s) computador (es) de destino devem estar online.
-   O usuário é responsável por replicar todos os dados não-COM + (por exemplo, tabelas de banco de dados, arquivos e assim por diante) para o (s) computador (es) de destino.
-   Os clusters podem participar da replicação, mas observe que COMREPL replica somente para computadores nomeados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Arquivos](file-management.md)
</dt> <dt>

[Registro em log e relatório de erros](logging-and-error-reporting.md)
</dt> <dt>

[Fases de replicação](replication-phases.md)
</dt> <dt>

[O que é replicado](what-gets-replicated.md)
</dt> </dl>

 

 



