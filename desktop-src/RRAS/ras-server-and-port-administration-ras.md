---
title: Administração de servidor e porta RAS
description: As funções de administração do servidor RAS permitem que você receba informações sobre um servidor RAS especificado e suas portas. Essas funções também permitem encerrar uma conexão em uma porta de servidor RAS especificada.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028796"
---
# <a name="ras-server-and-port-administration"></a>Administração de servidor e porta RAS

As funções de administração do servidor RAS permitem que você receba informações sobre um servidor RAS especificado e suas portas. Essas funções também permitem encerrar uma conexão em uma porta de servidor RAS especificada.

A [**função RasAdminServerGetInfo**](rasadminservergetinfo.md) retorna uma estrutura [**RAS SERVER \_ \_ 0**](ras-server-0-str.md) que contém informações sobre a configuração de um servidor RAS. As informações retornadas incluem o número de portas disponíveis atualmente para conexão, o número de portas atualmente em uso e o número de versão do servidor.

A [**função RasAdminPortEnum**](rasadminportenum.md) recupera uma matriz de estruturas [**RAS PORT \_ \_ 0**](ras-port-0-str.md) que contém informações para cada uma das portas configuradas em um servidor RAS. As informações de cada porta incluem:

-   O nome da porta
-   Informações sobre o dispositivo anexado à porta
-   Se o servidor RAS associado à porta é um servidor Windows NT/Windows 2000
-   Se a porta está em uso no momento e, se estiver, informações sobre a conexão

Você pode chamar a [**função RasAdminPortGetInfo**](rasadminportgetinfo.md) para obter informações adicionais sobre uma porta especificada em um servidor RAS. Essa função retorna uma [**estrutura RAS \_ PORT \_ 1**](ras-port-1-str.md) que contém uma estrutura [**RAS PORT \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informações adicionais sobre o estado atual da porta. A **função RasAdminPortGetInfo** também retorna uma matriz de [**estruturas RAS \_ PARAMETERS**](ras-parameters-str.md) que descrevem os valores de quaisquer chaves específicas de mídia associadas à porta. Uma **estrutura \_ RAS PARAMETERS** usa um valor da enumeração [**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md) para indicar o formato do valor para cada chave específica da mídia.

A [**função RasAdminPortGetInfo**](rasadminportgetinfo.md) também retorna uma estrutura [**RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) que contém vários contadores de estatística para a conexão atual, se for o caso, na porta. Para uma porta que faz parte de uma conexão multilink, **RasAdminPortGetInfo** retorna estatísticas para a porta individual e estatísticas cumulativas para todas as portas envolvidas na conexão. Você pode usar a [**função RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para redefinir os contadores de estatística para a porta. A [**função RasAdminPortDisconnect**](rasadminportdisconnect.md) desconecta uma porta que está em uso.

Use a [**função RasAdminFreeBuffer**](rasadminfreebuffer.md) para liberar memória alocada pelas funções [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo.**](rasadminportgetinfo.md) Use a [**função RasAdminGetErrorString**](rasadmingeterrorstring.md) para obter uma cadeia de caracteres que descreve um código de erro RAS retornado por uma das funções de administração de servidor RAS (RasAdmin).

 

 




