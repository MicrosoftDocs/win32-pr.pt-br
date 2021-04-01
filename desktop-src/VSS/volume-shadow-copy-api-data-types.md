---
description: 'Os seguintes tipos de dados são definidos na API de cópia de sombra de volume:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipos de dados da API de cópia de sombra de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647170"
---
# <a name="volume-shadow-copy-api-data-types"></a>Tipos de dados da API de cópia de sombra de volume

Os seguintes tipos de dados são definidos na API de cópia de sombra de volume:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>ID do VSS \_
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

A definição de **\_ ID do VSS** especifica o formato geral do identificador VSS. A **\_ ID do VSS** é um tipo de dados GUID padrão.

**VSS \_** Os s de ID são usados para identificar o seguinte: cópias de sombra, conjuntos de cópias de sombra, provedores, versões do provedor, gravadores (identificador de classe do gravador) e instâncias de gravadores.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

A definição de **\_ PWSZ do VSS** especifica uma cadeia de caracteres largo (WCHAR) terminada em nulo.

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_carimbo de data/hora VSS
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

A definição de **\_ carimbo de data/** hora do VSS mantém informações de carimbo de data/hora como um valor inteiro de 64 bits que contém o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC). Essa definição é intercambiável com a estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> </dl>

 

 
