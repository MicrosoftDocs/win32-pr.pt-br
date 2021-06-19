---
title: Tipos assinados e não assinados (MIDL)
description: Saiba mais sobre os tipos assinados e não assinados no MIDL. Os compiladores que usam tipos de padrões diferentes podem causar erros de software em seu aplicativo distribuído.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de dados MIDL, assinados e não assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407379"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipos assinados e não assinados (MIDL)

Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído. Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres como assinados ou não assinados. Observe que os compiladores de IDL do DCE não reconhecem a palavra-chave [**assinada**](signed.md). Portanto, esse recurso não está disponível quando você usa o compilador MIDL/opção **uso**

MIDL define o tipo [**pequeno**](small.md) para assumir o mesmo sinal padrão que o tipo [**Char**](char-idl.md) no compilador C de destino. Se o compilador assumir que **Char** não está assinado, **pequeno** também será definido como não assinado. Muitos compiladores do C permitem alterar o padrão como uma opção de linha de comando. Por exemplo, no ambiente de desenvolvimento Microsoft Visual C++, a opção de linha de comando **/j** altera o sinal padrão de **Char** de assinado para não assinado.

Você também pode controlar o sinal de variáveis do tipo [**Char**](char-idl.md) e [**Small**](small.md) com a opção de linha de comando [**/Char**](-char.md)do compilador MIDL. Essa opção permite que você especifique o sinal padrão usado pelo seu compilador. O compilador MIDL declara explicitamente o sinal de todos os tipos **Char** que não correspondem ao tipo padrão do compilador C no arquivo de cabeçalho gerado.

 

 




