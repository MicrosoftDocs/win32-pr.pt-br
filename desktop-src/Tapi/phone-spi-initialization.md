---
description: Como parte da abstração de dispositivo de telefone definida pelo TSPI, a TAPI e o provedor de serviços devem primeiro passar pela inicialização básica.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Inicialização do SPI do telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0c54e313c2be3846aeb604217f5324ec0d8a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761815"
---
# <a name="phone-spi-initialization"></a>Inicialização do SPI do telefone

Como parte da abstração de dispositivo de telefone definida pelo TSPI, a TAPI e o provedor de serviços devem primeiro passar pela inicialização básica. Essa inicialização básica é realizada para as metades da linha e do telefone da interface pelo mesmo conjunto de etapas. A primeira dessas etapas é a negociação de versão da interface. A TAPI executa isso chamando a função [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) . Essa função geralmente é usada para negociar em nome de um dispositivo de linha individual; dispositivos de linha diferentes dentro do mesmo provedor de serviços podem operar de acordo com versões de interface diferentes. A TAPI passa um valor de identificador de dispositivo reservado especial, [**Inicializa a \_ negociação**](initialize-negotiation.md), para indicar que está negociando uma versão de interface geral para funções de inicialização que afetam o provedor de serviços inteiro, tanto para linhas quanto para telefones.

O resultado dessa negociação é passado para os procedimentos subsequentes até que um dispositivo de telefone seja aberto. Nesse momento, o dispositivo de telefone se torna confirmado em uma versão de interface específica. Essa versão de interface é implícita até que o telefone seja fechado e não precisa ser passado para funções subsequentes que operam em um telefone aberto.

Seguindo a negociação de versão de interface geral, a TAPI chama a função [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) . Essa função inicializa o provedor de serviços, fornecendo também os parâmetros necessários para a operação subsequente. Esses parâmetros incluem o seguinte:

-   *dwPermanentProviderID*: especifica o identificador permanente do provedor de serviços que está sendo inicializado, exclusivo dentro dos provedores de serviço neste sistema.
-   *dwLineDeviceIDBase*: especifica o menor identificador de dispositivo para os dispositivos de linha com suporte por este provedor de serviços.
-   *dwPhoneDeviceIDBase*: especifica o menor identificador de dispositivo para os dispositivos de telefone com suporte por este provedor de serviços. Os dispositivos da classe de dispositivo de telefone de telefonia são identificados por inteiros começando de zero. Esse intervalo de identificadores é contíguo em todo o intervalo de dispositivos de telefone. Como pode haver vários provedores de serviços Gerenciando dispositivos de telefone em um único sistema, cada provedor de serviços Obtém uma parte contígua do intervalo total. Esse parâmetro informa ao provedor de serviços o menor valor em sua parte do intervalo. O provedor de serviços, em vez da TAPI, é responsável por mapear esse intervalo de variáveis para seus próprios identificadores de dispositivo internos. Isso dá ao fornecedor do provedor de serviços flexibilidade suficiente para usar identificadores de dispositivo em extensões específicas do dispositivo, se desejar. Como o provedor de serviços sabe quais identificadores de dispositivo aparecem em parâmetros e estruturas de dados definidos pela TAPI, ele pode usar identificadores de dispositivo consistentes em parâmetros de extensão específicos do dispositivo e estruturas de dados.
-   *dwNumLines*: especifica a quantos dispositivos de linha o provedor de serviços dá suporte.
-   *dwNumPhones*: especifica a quantos dispositivos de telefone esse provedor de serviços dá suporte.
-   *lpfnCompletionProc*: especifica o procedimento que o provedor de serviços chama para relatar a conclusão de todos os procedimentos operacionais assincronamente em dispositivos de linha e telefone.

[**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)a seguir, as operações normais, como a abertura de telefones, podem ser executadas.

 

 
