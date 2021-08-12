---
description: 'Os seguintes tipos de dados são definidos na API de Cópias de Sombra de Volume:'
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipos de dados da API de Cópia de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b159156c4a892ae7ad07a4d988bb8f32b0f5689a440fe3f31da3d6c15470675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590558"
---
# <a name="volume-shadow-copy-api-data-types"></a>Tipos de dados da API de Cópia de Sombra de Volume

Os seguintes tipos de dados são definidos na API de Cópias de Sombra de Volume:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>ID do \_ VSS
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

A **definição \_ de ID do VSS** especifica o formato geral do identificador VSS. A **\_ ID do VSS** é um tipo de dados GUID padrão.

**VSS \_ As IDs** são usadas para identificar o seguinte: cópias de sombra, conjuntos de cópias de sombra, provedores, versões do provedor, autores (identificador de classe do autor) e instâncias de autores.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

A **definição \_ do VSS PWSZ** especifica uma cadeia de caracteres largos terminada em nulo (wchar).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS \_ TIMESTAMP
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

A **definição \_ de TIMESTAMP** do VSS contém informações de carimbo de data/hora como um valor inteiro de 64 bits que contém o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC). Essa definição é intercambiável com a [**estrutura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

 

 
