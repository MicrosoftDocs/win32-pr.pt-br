---
description: Serviços de linha estendidos (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviço para a API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funções de linha estendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3531a63357276e6b2ea37365b5d5078d5c1de324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501743"
---
# <a name="extended-line-functions"></a>Funções de linha estendida

Serviços de linha estendidos (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviço para a API. A API define um mecanismo que permite aos fornecedores do provedor de serviços estender a TAPI usando extensões específicas do dispositivo. A API só define o mecanismo de extensão e, ao fazer isso, fornece acesso a extensões específicas do dispositivo, mas a API não define seu comportamento. O comportamento é completamente definido pelo provedor de serviços.

A TAPI consiste em definições de constante escalar e de sinalizador de bits, estruturas de dados, funções e mensagens. Os procedimentos são definidos para permitir que um fornecedor estenda a maioria deles da seguinte maneira.

Para constantes de dados escalares extensíveis, um fornecedor de provedor de serviços pode definir novos valores em um intervalo especificado. Como a maioria das constantes de dados são os s **DWORD**, normalmente, o intervalo 0x00000000 a 0x7FFFFFFF é reservado para extensões futuras comuns, enquanto 0X80000000 a 0xFFFFFFFF está disponível para extensões específicas do fornecedor. A suposição é que um fornecedor definiria valores que são extensões naturais dos tipos de dados definidos pela API.

Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados. Como a maioria das constantes de sinalizador de bits são os s **DWORD**, normalmente um número específico de bits inferiores é reservado para extensões comuns, enquanto os bits superiores restantes estão disponíveis para extensões específicas do fornecedor. Os sinalizadores de bits comuns são atribuídos do bit zero para cima; extensões específicas do fornecedor devem ser atribuídas do bit 31 para baixo. Isso fornece flexibilidade máxima na atribuição de posições de bits a extensões comuns versus extensões específicas do fornecedor. Um fornecedor deve definir novos valores que são extensões naturais dos sinalizadores de bits definidos pela API.

Estruturas de dados extensíveis têm um campo de tamanho de variavelmente reservado para uso específico do dispositivo. Sendo de tamanhos variados, o provedor de serviços decide a quantidade de informações e a interpretação. Um fornecedor que define um campo específico do dispositivo deve fazer essas extensões naturais da estrutura de dados original definida pela API.

Duas funções, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) e [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), e duas mensagens relacionadas, [**linha \_ DEVSPECIFIC**](line-devspecific.md) e [**\_ DEVSPECIFICFEATURE de linha**](line-devspecificfeature.md), fornecem um mecanismo de extensão específico do fornecedor. A função **lineDevSpecific** e a mensagem DEVSPECIFIC de linha associada \_ permitem que um aplicativo acesse os recursos de linha, endereço ou chamada específicos do dispositivo que não estão disponíveis com os serviços de telefonia básicos ou complementares. O perfil de parâmetro da função **lineDevSpecific** é genérico, pois essa pequena interpretação dos parâmetros é feita pela API. A interpretação dos parâmetros é definida pelo provedor de serviços e deve ser compreendida por um aplicativo que os utilize. Os parâmetros são simplesmente passados por meio da TAPI do aplicativo para o provedor de serviços. Um aplicativo que se baseia em extensões específicas do dispositivo geralmente não funcionará com outros provedores de serviços; no entanto, os aplicativos escritos nos serviços de telefonia básicos e complementares funcionarão com o provedor de serviços estendido.

Para sua conveniência, uma função de escape mais especializada também é fornecida. Ele é semelhante a [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), mas coloca a interpretação em alguns dos parâmetros. Essa função mais especializada é [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), uma função de escape específica do dispositivo para permitir o envio de recursos do comutador para o comutador. A linha de mensagem [**\_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) é a mensagem específica do dispositivo enviada ao aplicativo como uma indicação dos recursos enviados para o comutador. Essa função e sua mensagem associada permitem que um aplicativo eMule os pressionamentos de botão no telefone de recurso da linha. Como os telefones de recursos e os significados de seus botões são específicos do fornecedor, a invocação de recursos usando [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) também é específica do fornecedor.

Como mencionado anteriormente, não há registro central para identificadores de fabricantes. Em vez disso, um EXTIDGEN (gerador de identificador exclusivo) é disponibilizado.

 

 



