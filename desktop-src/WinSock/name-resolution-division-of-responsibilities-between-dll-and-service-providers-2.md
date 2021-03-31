---
title: Resolução de nomes para provedores de serviços e DLL
description: Os parágrafos a seguir descrevem como o \_32.dll Ws2 e os provedores de namespace implementam os serviços de resolução de nomes com suporte da API do Winsock.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b527f0849eb441ab7bc8d096c0198d703f2ce337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920906"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Resolução de nomes para provedores de serviços e DLL

Os parágrafos a seguir descrevem como o \_32.dll Ws2 e os provedores de namespace implementam os serviços de resolução de nomes com suporte da API do Winsock.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>Ws2 \_32.dll funcionalidade para resolução de nomes

O ws2 \_32.dll gerencia o registro e a demanda de carregamento de DLLs do provedor de namespace individual. Ele também é responsável por rotear operações de namespace de um aplicativo do Windows Sockets 2 para o conjunto apropriado de provedores de namespace. Esse mapeamento é regido pelo valor de namespace e parâmetros de identificador de provedor de serviço encontrados em funções de API individuais. Como regra geral, quando um provedor de namespace específico é referenciado, a operação é roteada apenas para um provedor identificado. Se o identificador do provedor de namespace for nulo, mas um namespace específico for referenciado, a operação será roteada para todos os provedores de namespace que dão suporte ao namespace identificado. Se o identificador do provedor de namespace for nulo e o identificador do namespace for fornecido como NS \_ All, a operação será roteada para todos os provedores de namespace ativos.

Como parte do início de uma consulta a um ou mais provedores de serviço, o ws2 \_32.dll aloca um objeto para controlar o estado de andamento da consulta. Um identificador opaco que representa esse objeto é retornado para o aplicativo que iniciou a consulta. O aplicativo fornece esse identificador como um parâmetro cada vez que chama repetidamente uma função de interface de aplicativo para recuperar a próxima unidade de dados resultante da consulta.

Em resposta a essas chamadas de procedimento de interface de aplicativo, o \_32.dll Ws2 usa as informações que ele armazena no objeto para fazer chamadas correspondentes aos provedores de namespace envolvidos na consulta. O ws2 \_32.dll atualiza as informações em seu objeto à medida que cada chamada de interface de aplicativo sucessiva ocorre para que as chamadas correspondentes aos provedores de namespace sejam progredidas adequadamente por todos os provedores de namespace envolvidos na consulta.

## <a name="namespace-provider-functionality"></a>Funcionalidade do provedor de namespace

Cada provedor de namespace é responsável por mapear o conjunto de funções que aparecem na SPI de resolução de nomes do Windows Sockets 2 para as transações apropriadas com o namespace com suporte. Em alguns casos, isso é basicamente uma questão de mapear o SPI para qualquer interface nativa existente para o namespace. Em outros, o provedor de namespace deve realizar transações com o provedor de namespace na rede. Alguns provedores de namespace farão isso fazendo chamadas para a API do Windows Sockets, outras usarão interfaces privadas para as pilhas de transporte associadas.

 

 



