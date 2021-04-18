---
description: A tabela DisplayToID relaciona a cadeia de caracteres amigável exibida pelo monitor do sistema ao GUID armazenado nas outras tabelas.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757090"
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

**Observação**  Antes do Windows Vista, os conjuntos de coletores de dados eram armazenados no registro em

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ logs queries**

. Os campos listados acima não correspondem aos valores no registro. Para o Windows Vista, os conjuntos de coletores de dados não são armazenados no registro.

 

 



