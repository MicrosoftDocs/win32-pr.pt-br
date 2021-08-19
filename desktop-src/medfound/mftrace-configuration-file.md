---
description: A ferramenta MFTrace pode ler um arquivo de configuração XML que especifica um ou mais provedores de rastreamento.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Arquivo de configuração MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871933"
---
# <a name="mftrace-configuration-file"></a>Arquivo de configuração MFTrace

A ferramenta [MFTrace](mftrace.md) pode ler um arquivo de configuração XML que especifica um ou mais provedores de rastreamento.

O elemento [**Providers**](providers.md) é o elemento raiz no arquivo de configuração.

## <a name="in-this-section"></a>Nesta seção

-   [**chaves**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**operador**](provider.md)
-   [**fornecedor**](providers.md)

## <a name="example"></a>Exemplo

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 



