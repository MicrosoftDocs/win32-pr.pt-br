---
title: Administração de porta e servidor RAS
description: As funções de administração do servidor RAS permitem que você obtenha informações sobre um servidor RAS especificado e suas portas. Essas funções também permitem que você encerre uma conexão em uma porta de servidor RAS especificada.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af21dfeda38a1c1147bf864a1fa1959092ac946
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005791"
---
# <a name="ras-server-and-port-administration"></a>Administração de porta e servidor RAS

As funções de administração do servidor RAS permitem que você obtenha informações sobre um servidor RAS especificado e suas portas. Essas funções também permitem que você encerre uma conexão em uma porta de servidor RAS especificada.

A função [**RasAdminServerGetInfo**](rasadminservergetinfo.md) retorna uma estrutura do [**\_ servidor RAS \_ 0**](ras-server-0-str.md) que contém informações sobre a configuração de um servidor RAS. As informações retornadas incluem o número de portas atualmente disponíveis para conexão, o número de portas atualmente em uso e o número de versão do servidor.

A função [**RasAdminPortEnum**](rasadminportenum.md) recupera uma matriz de estruturas da [**porta do RAS \_ \_ 0**](ras-port-0-str.md) que contém informações para cada uma das portas configuradas em um servidor RAS. As informações para cada porta incluem:

-   O nome da porta
-   Informações sobre o dispositivo conectado à porta
-   Se o servidor RAS associado à porta é um servidor Windows NT/Windows 2000
-   Se a porta está em uso no momento e, se for, informações sobre a conexão

Você pode chamar a função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) para obter informações adicionais sobre uma porta especificada em um servidor RAS. Essa função retorna uma estrutura de [**\_ porta \_ 1 RAS**](ras-port-1-str.md) que contém uma estrutura de [**porta de acesso remoto \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informações adicionais sobre o estado atual da porta. A função **RasAdminPortGetInfo** também retorna uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) que descrevem os valores de qualquer chave específica de mídia associada à porta. Uma estrutura de **\_ parâmetros de Ras** usa um valor da enumeração de [**\_ \_ formato de params de Ras**](ras-params-format-str.md) para indicar o formato do valor para cada chave específica de mídia.

A função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) também retorna uma estrutura de [**\_ \_ Estatísticas de porta RAS**](ras-port-statistics-str.md) que contém vários contadores de estatística para a conexão atual, se houver, na porta. Para uma porta que faz parte de uma conexão Multilink, **RasAdminPortGetInfo** retorna estatísticas para a porta individual e estatísticas cumulativas para todas as portas envolvidas na conexão. Você pode usar a função [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para redefinir os contadores de estatística para a porta. A função [**RasAdminPortDisconnect**](rasadminportdisconnect.md) desconecta uma porta que está em uso.

Use a função [**RasAdminFreeBuffer**](rasadminfreebuffer.md) para liberar memória alocada pelas funções [**RasAdminPortEnum**](rasadminportenum.md) e [**RasAdminPortGetInfo**](rasadminportgetinfo.md) . Use a função [**RasAdminGetErrorString**](rasadmingeterrorstring.md) para obter uma cadeia de caracteres que descreve um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin).

 

 




