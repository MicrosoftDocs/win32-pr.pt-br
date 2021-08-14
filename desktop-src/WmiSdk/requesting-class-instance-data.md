---
description: 'As consultas de dados são instruções WQL que solicitam instâncias de classes. Para emitir uma consulta de dados, os aplicativos chamam o método IWbemServices:: ExecQuery ou IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Solicitando dados de instância de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316283"
---
# <a name="requesting-class-instance-data"></a>Solicitando dados de instância de classe

As consultas de dados são instruções WQL que solicitam instâncias de classes. Para emitir uma consulta de dados, os aplicativos chamam o método [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) ou [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .

As instruções a seguir são usadas para fazer consultas de dados:

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIADORES DE](associators-of-statement.md)
-   [REFERÊNCIAS DE](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

a instrução WQL SELECT é a instrução de linguagem SQL padrão (SQL) para recuperar informações, com algumas restrições e extensões específicas do WQL. embora a instrução SQL SELECT seja normalmente usada no ambiente de banco de dados para recuperar colunas específicas de tabelas, a instrução WQL SELECT é usada no WMI para recuperar instâncias de uma única classe. O WQL não oferece suporte a consultas em várias classes.

Os ASSOCIAdores de e referências de instruções são específicos do WQL e não fazem parte do SQL padrão. A instrução ASSOCIATORS OF recupera todas as instâncias de classe associadas a uma instância de classe de origem específica e referências de recupera todas as instâncias que se referem a uma instância de origem específica. As associações são representadas por instâncias de uma [classe de associação](declaring-an-association-class.md).

 

 



