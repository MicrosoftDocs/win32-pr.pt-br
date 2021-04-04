---
title: Tipos assinados e não assinados (RPC)
description: Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824120"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipos assinados e não assinados (RPC)

Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído. Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres como **assinados** ou **não assinados**.

MIDL define o tipo [**pequeno**](/windows/desktop/Midl/small) para assumir o mesmo sinal padrão que o tipo **Char** no compilador C de destino. Se o compilador assumir que **Char** não está assinado, **pequeno** também será definido como não assinado. Muitos compiladores do C permitem alterar o padrão como uma opção de linha de comando. Por exemplo, a opção de linha de comando Microsoft C Compiler **/j** altera o sinal padrão de **Char** de assinado para não assinado.

Você também pode controlar o sinal de variáveis do tipo **Char** e **Small** com a opção de linha de comando [**/Char**](/windows/desktop/Midl/-char)do compilador MIDL. Essa opção permite que você especifique o sinal padrão usado pelo seu compilador. O compilador MIDL declara explicitamente o sinal de todos os tipos **Char** que não correspondem ao tipo padrão do compilador C no arquivo de cabeçalho gerado.

 

 
