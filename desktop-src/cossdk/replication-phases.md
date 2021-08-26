---
description: COMREPL faz seu trabalho em três fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d1924b85e2681854fe8de604fea1fe59a022fa97843051457677905048dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990416"
---
# <a name="replication-phases"></a>Fases de replicação

COMREPL faz seu trabalho em três fases. O processo de replicação é dividido em fases distintas pelos dois seguintes motivos:

-   Para separar o trabalho feito para preparar a origem do trabalho que é feito em cada destino
-   Para atrasar a modificação do destino até que todos os dados foram adquiridos da origem

As fases de replicação são as a seguir.



| Fase         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase de preparo | Exporta todos os aplicativos instalados localmente no computador de origem. Essa fase não toca na configuração de nenhum destino.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase de cópia    | Copia dados para um computador de destino. Todos os aplicativos exportados na origem são copiados para o destino. Essa é uma operação de cópia de arquivo. (Consulte [Gerenciamento de Arquivos](file-management.md).) Esta etapa também adquire alguns dados do computador de origem que não são encapsulados em arquivos de aplicativo exportados (por exemplo, identidades de aplicativo). Esses dados são mantidos na memória dentro de COMREPL. Essa fase não toca na configuração de nenhum computador de destino.                                                                               |
| Fase de instalação | Instala o catálogo de origem em um computador de destino. Quando essa etapa é iniciada, todos os dados necessários para reconfigurar o destino estão dentro de arquivos de aplicativo no sistema de arquivos do destino ou são mantidos como dados de instância no COMREPL. Essa fase excluirá todos os aplicativos instalados no destino (exceto os aplicativos descritos em [What Gets Replicated](what-gets-replicated.md)) antes de instalar os aplicativos copiados da origem. O COMREPL é instalado em vários destinos simultaneamente usando um thread de instalação por destino. |



 

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

 

 



