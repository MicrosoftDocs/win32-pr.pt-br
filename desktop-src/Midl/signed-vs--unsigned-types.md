---
title: Tipos assinados e não assinados (MIDL)
description: Saiba mais sobre tipos assinados e não assinados em MIDL. Compiladores que usam tipos de padrões diferentes podem causar erros de software em seu aplicativo distribuído.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipos de dados MIDL, assinados e não assinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9f65931720e80de6575d8b7125e6b5082a32e510e1be07e620e6592d30e485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066746"
---
# <a name="signed-and-unsigned-types-midl"></a>Tipos assinados e não assinados (MIDL)

Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído. Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres como assinados ou não assinados. Observe que os compiladores de IDL de DCE não reconhecem a palavra-chave [**signed**](signed.md). Portanto, esse recurso não está disponível quando você usa a opção de **compilador/osf** MIDL.

MIDL define o [**tipo pequeno**](small.md) para assumir o mesmo sinal padrão que o tipo [**char**](char-idl.md) no compilador C de destino. Se o compilador assumir que **char** não foi assinado, **small** também será definido como unsigned. Muitos compiladores C permitem alterar o padrão como uma opção de linha de comando. Por exemplo, no ambiente Microsoft Visual C++ de desenvolvimento, a opção de linha de comando **/J** altera o sinal padrão de **char** de assinado para não assinado.

Você também pode controlar o sinal de variáveis do tipo [**char**](char-idl.md) e [**small**](small.md) com a opção de linha de comando do compilador MIDL [**/char**](-char.md). Essa opção permite que você especifique o sinal padrão usado pelo compilador. O compilador MIDL declara explicitamente o sinal de todos os tipos **de caracteres** que não corresponderem ao tipo padrão do compilador C no arquivo de header gerado.

 

 




