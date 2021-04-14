---
title: Sobre a administração de porta e servidor RAS
description: As funções de administração do servidor RAS obtêm informações sobre um servidor RAS especificado e suas portas. Essas funções também são usadas para encerrar uma conexão em uma porta de servidor RAS especificada.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- Administração de RAS RRAS, gerenciamento de porta e servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104453802"
---
# <a name="about-ras-server-and-port-administration"></a>Sobre a administração de porta e servidor RAS

As funções de administração do servidor RAS obtêm informações sobre um servidor RAS especificado e suas portas. Essas funções também são usadas para encerrar uma conexão em uma porta de servidor RAS especificada.

A função [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) retorna uma estrutura de [**servidor de MPR \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) que contém informações sobre a configuração de um servidor RAS. As informações retornadas incluem o número de portas atualmente disponíveis para conexões, o número de portas atualmente em uso e o número de versão do servidor.

A função [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) recupera uma matriz de estruturas da [**porta do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) . Cada estrutura contém informações para uma das portas configuradas em um servidor RAS. As informações para cada porta incluem:

-   O nome da porta
-   Informações sobre o dispositivo conectado à porta
-   Se o servidor RAS associado à porta é um servidor Windows NT/Windows 2000
-   Se a porta está em uso no momento e, se for, informações sobre a conexão

Para obter as portas em uso por uma conexão específica, passe [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) um identificador para essa conexão no parâmetro *hConnection* . Para obter um identificador para uma conexão, use a função [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) . Como alternativa, se você tiver implementado uma [dll de administração de Ras](ras-administration-dll.md), as funções [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) e [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) receberão um identificador para cada nova conexão no momento em que a conexão for estabelecida.

Você pode chamar a função [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) para obter informações adicionais sobre uma porta especificada em um servidor RAS. Essa função retorna uma estrutura de [**\_ porta \_ 1 RAS**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) que contém uma estrutura de [**porta de acesso remoto \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) e informações adicionais sobre o estado atual da porta. A função [**RasAdminPortGetInfo**](rasadminportgetinfo.md) também retorna uma matriz de estruturas de [**\_ parâmetros de Ras**](ras-parameters-str.md) que descrevem os valores de qualquer chave específica de mídia associada à porta. Uma estrutura de **\_ parâmetros de Ras** usa um valor da enumeração de [**\_ \_ formato de params de Ras**](ras-params-format-str.md) para indicar o formato do valor para cada chave específica de mídia.

A função [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) também retorna uma estrutura de [**\_ \_ Estatísticas de porta RAS**](ras-port-statistics-str.md) que contém vários contadores de estatística para a conexão atual, se houver, na porta. Para uma porta que faz parte de uma conexão Multilink, **MprAdminPortGetInfo** retorna estatísticas para a porta individual e estatísticas cumulativas para todas as portas envolvidas na conexão. Você pode usar a função [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) para redefinir os contadores de estatística para a porta. A função [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) desconecta uma porta que está em uso.

Use a função [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) para liberar memória alocada pelas funções [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) e [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) . Use a função [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) para obter uma cadeia de caracteres que descreve um código de erro RAS retornado por uma das funções de administração do servidor RAS (RasAdmin).

 

 




