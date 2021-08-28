---
description: Como parte da abstração do dispositivo de telefone definida pelo TSPI, a TAPI e o provedor de serviços devem primeiro passar pela inicialização básica.
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Telefone Inicialização da SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88465e31857ee9ecc3a54f98f98bf6d1d3b50b837d845dbf36af08be0ec78a7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072886"
---
# <a name="phone-spi-initialization"></a>Telefone Inicialização da SPI

Como parte da abstração do dispositivo de telefone definida pelo TSPI, a TAPI e o provedor de serviços devem primeiro passar pela inicialização básica. Essa inicialização básica é realizada para as metades de linha e telefone da interface pelo mesmo conjunto de etapas. A primeira dessas etapas é a negociação de versão da interface. A TAPI executa isso chamando a [**função TSPI \_ lineNegotiateTSPIVersion.**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) Essa função geralmente é usada para negociar em nome de um dispositivo de linha individual; diferentes dispositivos de linha dentro do mesmo provedor de serviços podem operar de acordo com versões de interface diferentes. A TAPI passa um valor especial do identificador de dispositivo reservado, [**INITIALIZE \_ NEGOTIATION,**](initialize-negotiation.md)para indicar que está negociando uma versão geral da interface para funções de inicialização que afetam todo o provedor de serviços, tanto para linhas quanto para telefones.

O resultado dessa negociação é passado para procedimentos subsequentes até que um dispositivo de telefone seja aberto. Nesse momento, o dispositivo de telefone se torna confirmado em uma versão de interface específica. Essa versão da interface é implícita até que o telefone seja fechado e não precise ser passada para funções subsequentes que operam em um telefone aberto.

Após a negociação geral da versão da interface, a TAPI chama a [**função TSPI \_ providerInit.**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) Essa função inicializa o provedor de serviços, também dando a ele os parâmetros necessários para a operação subsequente. Esses parâmetros incluem o seguinte:

-   *dwPermanentProviderID:* especifica o identificador permanente do provedor de serviços que está sendo inicializado, exclusivo dentro dos provedores de serviços nesse sistema.
-   *dwLineDeviceIDBase:* especifica o identificador de dispositivo mais baixo para os dispositivos de linha compatíveis com esse provedor de serviços.
-   *dwPhoneDeviceIDBase:* especifica o identificador de dispositivo mais baixo para os dispositivos de telefone compatíveis com esse provedor de serviços. Os dispositivos da classe de dispositivo de telefonia são identificados por inteiros começando do zero. Esse intervalo de identificadores é contíguo em toda a gama de dispositivos de telefone. Como pode haver vários provedores de serviços gerenciando dispositivos de telefone em um único sistema, cada provedor de serviços obtém uma parte contígua do intervalo total. Esse parâmetro informa ao provedor de serviços o valor mais baixo em sua parte do intervalo. O provedor de serviços, em vez de TAPI, é responsável por mapear esse intervalo de variáveis para seus próprios identificadores de dispositivo internos. Isso oferece ao fornecedor do provedor de serviços flexibilidade suficiente para usar identificadores de dispositivo em extensões específicas do dispositivo, se quiser. Como o provedor de serviços sabe quais identificadores de dispositivo aparecem em estruturas de dados e parâmetros definidos por TAPI, ele pode usar identificadores de dispositivo consistentes em estruturas de dados e parâmetros de extensão específicos do dispositivo.
-   *dwNumLines:* especifica quantos dispositivos de linha esse provedor de serviços dá suporte.
-   *dwNumPhones:* especifica quantos dispositivos de telefone esse provedor de serviços dá suporte.
-   *lpfnCompletionProc:* especifica o procedimento que o provedor de serviços chama para relatar a conclusão de todos os procedimentos operacionais assíncronos em dispositivos de linha e telefone.

Após [**o provedor TSPIInit \_**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), operações normais, como abrir telefones, podem ser executadas.

 

 
