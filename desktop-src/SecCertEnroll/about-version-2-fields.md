---
description: Um certificado X.509 versão 2 contém os campos básicos definidos na versão 1 e adiciona os campos a seguir.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Campos da versão 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164250"
---
# <a name="version-2-fields"></a>Campos da versão 2

Um certificado X.509 versão 2 contém os campos básicos definidos na versão 1 e adiciona os campos a seguir.

## <a name="issuer-unique-identifier"></a>Identificador Exclusivo de Emissor

Contém um valor exclusivo que pode ser usado para tornar o nome X.500 da AC não ambíguo quando reutilizado por entidades diferentes com o tempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Identificador Exclusivo de Entidade

Contém um valor exclusivo que pode ser usado para tornar o nome X.500 da entidade do certificado não ambíguo quando reutilizado por entidades diferentes com o tempo.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Campos básicos](about-basic-fields.md)
</dt> <dt>

[Extensões da versão 3](about-version-3-extensions.md)
</dt> <dt>

[Certificados de chave pública X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



