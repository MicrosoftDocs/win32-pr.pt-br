---
description: A tabela DisplayToID relaciona a cadeia de caracteres amigável exibida pelo monitor do sistema ao GUID armazenado nas outras tabelas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485eab24a2c758b36e190e035a9442a032ebd683f3f5ea052bd37992ad14c85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033906"
---
# <a name="displaytoid"></a>DisplayToID

A tabela **DisplayToID** relaciona a cadeia de caracteres amigável exibida pelo monitor do sistema ao GUID armazenado nas outras tabelas.

A tabela **DisplayToID** define os seguintes campos:

-   **GUID:** Identificador exclusivo gerado para um log. Este campo é a chave primária desta tabela.
-   **RunId:** Reservado para uso interno.
-   **DisplayString:** Nome do arquivo de log, conforme exibido no monitor do sistema.
-   **LogStartTime:** Hora em que o processo de log foi iniciado no formato aaaa-mm-dd hh: mm: SS: nnn.
-   **LogStopTime:** Tempo que o processo de log parou no formato aaaa-mm-dd hh: mm: SS: nnn. Vários arquivos de log com o mesmo valor de **TipoDeExibição** podem ser diferenciados usando o valor nesse e nos campos **LogStartTime** . Os valores nos campos **LogStartTime** e **LogStopTime** também permitem que o tempo total da coleção seja acessado rapidamente.
-   **NumberOfRecords:** Número de amostras armazenadas na tabela para cada coleção de logs.
-   **MinutesToUTC:** Valor usado para converter os dados de linha armazenados na hora UTC para a hora local.
-   **TimeZoneName:** Nome do fuso horário em que os dados foram coletados. Se você estiver coletando ou tiver dados reconectados de um arquivo coletado em sistemas em seu próprio fuso horário, esse campo irá declarar o local.

**Observação**  antes do Windows Vista, os conjuntos de coletores de dados eram armazenados no registro em

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ logs queries**

. Os campos listados acima não correspondem aos valores no registro. para o Windows Vista, os conjuntos de coletores de dados não são armazenados no registro.

 

 



