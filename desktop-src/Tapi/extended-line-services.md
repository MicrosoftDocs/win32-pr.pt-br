---
description: Serviços de linha estendidos (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviço para TSPI.
ms.assetid: 23519d23-27bd-422e-b3c4-00e0d0d93f9e
title: Serviços de linha estendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1ce08d25633d33fd518d8686271c198ca5034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779313"
---
# <a name="extended-line-services"></a>Serviços de linha estendida

Serviços de linha estendidos (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviço para TSPI. TSPI define um mecanismo que permite aos fornecedores do provedor de serviços estender o SPI de telefonia usando extensões específicas do dispositivo. TSPI define apenas o mecanismo de extensão e, ao fazer isso, fornece acesso a extensões específicas do dispositivo, mas o TSPI não define seu comportamento. O comportamento é completamente definido pelo provedor de serviços.

O SPI de telefonia consiste em definições de constante escalar e de sinalizador de bits, estruturas de dados, funções e mensagens de retorno de chamada. Os procedimentos são definidos para permitir que um fornecedor estenda a maioria deles da seguinte maneira.

Para constantes de dados escalares extensíveis, um fornecedor de provedor de serviços pode definir novos valores em um intervalo especificado. Como a maioria das constantes de dados são os s **DWORD**, normalmente, o intervalo 0x00000000 a 0x7FFFFFFF é reservado para extensões futuras comuns, enquanto 0X80000000 a 0xFFFFFFFF está disponível para extensões específicas do fornecedor. A suposição é que um fornecedor definiria valores que são extensões naturais dos tipos de datatipos definidos por TSPI.

Para constantes de dados de sinalizador de bit extensível, um fornecedor de provedor de serviço pode definir novos valores para bits especificados. Como a maioria das constantes de sinalizador de bit são os s **DWORD**, normalmente um número específico dos bits inferiores é reservado para extensões comuns, enquanto os bits superiores restantes estão disponíveis para extensões específicas do fornecedor. Os sinalizadores de bits comuns são atribuídos do bit zero para cima; extensões específicas do fornecedor devem ser atribuídas do bit 31 para baixo. Isso fornece flexibilidade máxima na atribuição de posições de bits a extensões comuns versus extensões específicas do fornecedor. Um fornecedor deve definir novos valores que são extensões naturais dos sinalizadores de bits definidos por TSPI.

Estruturas de dados extensíveis têm um campo de tamanho de variavelmente reservado para uso específico do dispositivo. Sendo de tamanhos variados, o provedor de serviços decide a quantidade de informações e a interpretação. Um fornecedor que define um campo específico do dispositivo deve fazer essas extensões naturais da estrutura de dados original definida por TSPI.

Duas funções, [**TSPI \_ LineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) e [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)e quatro mensagens relacionadas, [**line \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)), [**line \_ CALLDEVSPECIFIC**](line-calldevspecific.md), line [**\_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))e [**line \_ CALLDEVSPECIFICFEATURE**](line-calldevspecificfeature.md), oferecem um mecanismo de extensão específico do fornecedor. A operação **TSPI \_ lineDevSpecific** e \_ as mensagens DEVSPECIFIC de linha associadas e CALLDEVSPECIFIC de linha \_ permitem que o aplicativo cliente do Tapi32.dll acesse a linha específica do dispositivo, o endereço ou os recursos de chamada que não estão disponíveis nos serviços de telefonia básicos ou complementares. O perfil de parâmetro da função [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) é genérico, pois a pequena interpretação dos parâmetros é feita pelo TSPI. Os parâmetros de identificador de dispositivo têm significados definidos pelo TSPI e são convertidos adequadamente entre o aplicativo e o provedor de serviços. Os parâmetros genéricos são simplesmente passados por meio de não modificado. A interpretação dos parâmetros genéricos é definida pelo provedor de serviços e deve ser compreendida por qualquer aplicativo que os utilize. Um aplicativo que se baseia em extensões específicas do dispositivo geralmente não funciona com outros provedores de serviço. No entanto, os aplicativos escritos inteiramente nos serviços de telefonia básicos e complementares devem funcionar com o provedor de serviços estendido.

A implementação de TAPI das funções e mensagens específicas do dispositivo é "passagem". A TAPI não examina nem modifica os parâmetros e buffers específicos de dispositivos genéricos, mas mapeia valores de identificador opaco no nível de aplicativo (usados no nível de TAPI) para valores de identificador opaco de nível de provedor de serviço (usados no nível de TSPI).

Em relação à conversão de identificadores, a natureza de passagem das partes genéricas das extensões específicas do dispositivo tem uma consequência importante. Um provedor de serviços não tem como relacionar os identificadores usados no nível de TSPI para aqueles no nível de TAPI, exceto passando-os pelos parâmetros e campos de identificador predefinidos. Qualquer identificador colocado na área de extensão genérica é não traduzido pela TAPI conforme é passado entre o aplicativo e o provedor de serviços. O designer de uma extensão de provedor de serviço geralmente não deve definir extensões que passem identificadores dessa maneira.

A abordagem apropriada ao definir uma extensão específica do dispositivo que deve se referir a dispositivos específicos sem usar identificadores é fazer referência a eles usando sua identificação de dispositivo absoluta. O identificador de dispositivo usado na abertura de uma linha no nível de TAPI, por exemplo, é estritamente o mesmo valor que é usado no nível de TSPI para abrir a linha. Da mesma forma, uma tupla (identificador de dispositivo de linha, identificador de endereço) que identifica exclusivamente um endereço no nível de TAPI usa os mesmos valores para identificar a mesma coisa no nível de TSPI.

Para sua conveniência, uma função de escape mais especializada também é fornecida. É semelhante a [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific), mas coloca a interpretação em alguns dos parâmetros. A função [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) e as mensagens [**\_ DEVSPECIFICFEATURE de linha**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) associadas e [**\_ CALLDEVSPECIFICFEATURE de linha**](line-calldevspecificfeature.md) permitem que a TAPI eMule os pressionamentos de botão no telefone de recurso da linha. Como os telefones de recursos e os significados de seus botões são específicos do fornecedor, a invocação de recursos usando **TSPI \_ lineDevSpecificFeature** também é específica do fornecedor.

Para resumir, a função [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) é uma função de escape específica do dispositivo para permitir o envio de recursos do comutador para o comutador. A [**linha \_ CALLDEVSPECIFICFEATURE**](line-calldevspecificfeature.md) Message é uma mensagem específica do dispositivo enviada para o retorno de chamada do aplicativo como uma indicação de recursos relacionados à chamada enviados ao comutador. [**Linha \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) é uma mensagem específica do dispositivo enviada para o retorno de chamada do aplicativo como uma indicação de recursos relacionados à linha enviados para o comutador.

Não há registro central para identificadores de fabricantes. Em vez disso, um gerador de identificador exclusivo chamado Extidgen.exe é disponibilizado como parte do TSPI. O fornecedor que projeta um conjunto de extensões específicas do dispositivo usa esse utilitário para obter um identificador exclusivo para essas extensões.

 

 
