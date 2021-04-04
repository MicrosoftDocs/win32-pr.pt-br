---
title: Usar o sinalizador/robust
description: Sempre compile arquivos. idl usando a opção/robust
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917443"
---
# <a name="use-the-robust-flag"></a>Usar o sinalizador/robust

Sempre compile arquivos. idl usando a opção [**/robust**](/windows/desktop/Midl/-robust) O uso da opção **/robust** gera informações adicionais que permitem que o mecanismo de representação de dados de rede (NDR) execute a verificação de erros em tempo de execução em argumentos correlacionados em matrizes dinâmicas, uniões e ponteiros de interface em aplicativos com e RPC. Se o software não conseguir compilar com esse sinalizador, o software será tão exposto a ataques que nenhum esforço em nenhuma outra área poderá protegê-lo.

 

 