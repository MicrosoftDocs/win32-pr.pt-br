---
description: A tabela de comDados contém uma linha para cada contador que é coletada em um momento específico. Haverá um grande número dessas linhas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828393"
---
# <a name="counterdata"></a>Dados

A tabela de **comDados** contém uma linha para cada contador que é coletada em um momento específico. Haverá um grande número dessas linhas.

A tabela de **comDados** define os seguintes campos:

-   **GUID:** GUID para este conjunto de dados. Use essa chave para ingressar com a tabela [**DisplayToID**](displaytoid.md) .
-   **Counterid:** Identifica o contador. Use essa chave para ingressar com a tabela de [**detalhes**](counterdetails.md) .
-   **RecordIndex:** O índice de exemplo para um identificador de contador e GUID de coleção específicos. O valor aumenta para cada exemplo sucessivo nesse arquivo de log.
-   **DateTime:** A hora em que a coleção foi iniciada, em hora UTC.
-   **Valor:** O valor formatado do contador. Esse valor pode ser zero para o primeiro registro se o contador exigir dois exemplos para computar um valor de exibição.
-   **FirstValueA:** Combine esse valor de 32 bits com o valor de **FirstValueB** para criar o membro **primeirovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA** contém os bits de ordem inferior.
-   **FirstValueB:** Combine esse valor de 32 bits com o valor de **FirstValueA** para criar o membro **primeirovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB** contém os bits de ordem superior.
-   **SecondValueA:** Combine esse valor de 32 bits com o valor de **SecondValueB** para criar o membro **segundovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contém os bits de ordem inferior.
-   **SecondValueB:** Combine esse valor de 32 bits com o valor de **SecondValueA** para criar o membro **segundovalue** do [**\_ \_ contador bruto de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contém os bits de ordem superior.

Os campos **GUID**, **counterid** e **RecordIndex** compõem a chave primária desta tabela.

 

 



