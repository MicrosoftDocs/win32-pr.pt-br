---
title: Tipos assinados e não assinados (RPC)
description: Saiba mais sobre tipos assinados e não assinados no RPC. Compiladores que usam tipos de padrões diferentes podem causar erros de software em seu aplicativo distribuído.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406539"
---
# <a name="signed-and-unsigned-types-rpc"></a>Tipos assinados e não assinados (RPC)

Compiladores que usam padrões diferentes para tipos assinados e não assinados podem causar erros de software em seu aplicativo distribuído. Você pode evitar esses problemas declarando explicitamente seus tipos de caracteres **como assinados** **ou sem sinal.**

MIDL define o [**tipo pequeno**](/windows/desktop/Midl/small) para assumir o mesmo sinal padrão que o tipo **char** no compilador C de destino. Se o compilador assumir que **char** não foi assinado, **small** também será definido como sem-assinatura. Muitos compiladores C permitem alterar o padrão como uma opção de linha de comando. Por exemplo, a opção de linha de comando **/J** do compilador do Microsoft C altera o sinal padrão de **char** de assinado para não assinado.

Você também pode controlar o sinal de variáveis do tipo **char** e **small** com a opção de linha de comando do compilador MIDL [**/char**](/windows/desktop/Midl/-char). Essa opção permite que você especifique o sinal padrão usado pelo compilador. O compilador MIDL declara explicitamente o sinal de todos os tipos **de caracteres** que não corresponderem ao tipo padrão do compilador C no arquivo de header gerado.

 

 
