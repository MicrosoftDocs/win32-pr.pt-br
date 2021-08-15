---
title: Usar o sinalizador /robust
description: Sempre compile arquivos .idl usando a opção /robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010884"
---
# <a name="use-the-robust-flag"></a>Usar o sinalizador /robust

Sempre compile arquivos .idl usando a [**opção /robust.**](/windows/desktop/Midl/-robust) O uso da opção **/robust** gera informações adicionais que permitem que o mecanismo de NDR (Representação de Dados de Rede) execute a verificação de erro em tempo de execução em argumentos correlacionados em matrizes dinâmicas, uniões e ponteiros de interface de saída em aplicativos COM e RPC. Se o software não for compilado com esse sinalizador, o software será tão exposto a ataques que nenhum esforço em nenhuma outra área poderá protegê-lo.

 

 