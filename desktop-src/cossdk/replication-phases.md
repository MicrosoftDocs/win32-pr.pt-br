---
description: COMREPL faz seu trabalho em três fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813763"
---
# <a name="replication-phases"></a>Fases de replicação

COMREPL faz seu trabalho em três fases. O processo de replicação é dividido em fases distintas pelos dois motivos a seguir:

-   Para separar o trabalho feito para preparar a origem do trabalho que é feito em cada destino
-   Para atrasar a modificação do destino até que todos os dados tenham sido adquiridos da origem

As fases de replicação são as seguintes.



| Fase         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase de preparo | Exporta todos os aplicativos instalados localmente no computador de origem. Essa fase não toca na configuração de nenhum destino.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase de cópia    | Copia dados para um computador de destino. Todos os aplicativos exportados na origem são copiados para o destino. Esta é uma operação de cópia de arquivo. (Consulte [Gerenciamento de arquivos](file-management.md).) Essa etapa também adquire alguns dados do computador de origem que não estão encapsulados em arquivos de aplicativo exportados (por exemplo, identidades de aplicativo). Esses dados são mantidos na memória no COMREPL. Essa fase não toca na configuração de nenhum computador de destino.                                                                               |
| Fase de instalação | Instala o catálogo de origem em um computador de destino. Quando essa etapa é iniciada, todos os dados necessários para reconfigurar o destino estão dentro dos arquivos de aplicativo no sistema de arquivos do destino ou são mantidos como dados de instância no COMREPL. Esta fase excluirá todos os aplicativos instalados no destino (exceto os aplicativos descritos em [o que é replicado](what-gets-replicated.md)) antes da instalação dos aplicativos copiados da origem. O COMREPL é instalado em vários destinos simultaneamente usando um thread de instalação por destino. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de Arquivos](file-management.md)
</dt> <dt>

[Registro em log e relatório de erros](logging-and-error-reporting.md)
</dt> <dt>

[Usando COMREPL](using-comrepl.md)
</dt> <dt>

[O que é replicado](what-gets-replicated.md)
</dt> </dl>

 

 



