---
description: A tabela de detalhes descreve um contador específico em um determinado computador.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: Detalhes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef429f7f90c38d53f085ed0243e1c799c1d1cfa808c7aa052d8a37ed3a1faf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011354"
---
# <a name="counterdetails"></a>Detalhes

A tabela de **detalhes** descreve um contador específico em um determinado computador.

A tabela de **detalhes** define os seguintes campos:

-   **Counterid:** Um identificador exclusivo no banco de dados que é mapeado para uma cadeia de caracteres de texto de nome de contador específico. Este campo é a chave primária desta tabela.
-   **MachineName:** O nome do computador que registrou esse conjunto de dados.
-   **ObjectName:** O nome do objeto de desempenho.
-   **CounterName:** O nome do contador.
-   **Tipoy:** O tipo de contador. para obter uma lista de tipos de contadores e suas fórmulas, consulte a seção tipos de contadores do [Kit de implantação do Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DefaultScale:** O dimensionamento padrão a ser aplicado aos dados brutos do contador de desempenho.
-   **InstanceName:** O nome da instância do contador.
-   **InstanceIndex:** O número de índice da instância do contador.
-   **ParentName:** Alguns contadores são logicamente associados a outras pessoas e são chamados de pais. Por exemplo, o pai de um thread é um processo e o pai de um driver de disco lógico é uma unidade física. Este campo contém o nome do pai. O valor neste campo ou o campo **ParentObjectID** identifica uma instância pai específica. Se o valor nesse campo for **nulo**, o valor no campo **ParentObjectID** deverá ser verificado para identificar o pai. Se os valores em ambos os campos forem **nulos**, o contador não terá um pai.
-   **ParentObjectID:** O identificador exclusivo do pai. O valor desse campo ou **painame** identifica uma instância pai específica. Se o valor nesse campo for **nulo**, o valor no campo **parentName** deverá ser verificado para identificar o pai.

 

 
