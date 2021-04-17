---
description: O controle de dispositivo no nível de aplicativo do usuário final ou do servidor requer um conjunto relativamente pequeno de informações básicas.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Controle de dispositivo (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17336941a55a529c6b436270f7b225a1cada3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779910"
---
# <a name="device-control-telephony-api"></a>Controle de dispositivo (API de telefonia)

O controle de dispositivo no nível de aplicativo do usuário final ou do servidor requer um conjunto relativamente pequeno de informações básicas. A camada de abstração do provedor de serviços executa o controle detalhado do dispositivo. Os provedores de serviços relatam informações de dispositivo necessárias a um aplicativo por meio da TAPI.

As principais categorias de dispositivo incluem:

-   [Rede](network-ovr.md): a camada de transporte para comunicações. Do ponto de vista de um aplicativo, as informações sobre a rede normalmente são inseridas no tipo de endereço, como LINEADDRESSTYPE \_ PHONENUMBER.
-   [Linha](line-ovr.md): uma conexão a uma rede. Esse conceito é muito usado na TAPI 2,2 (TAPI/C).
-   [Canal](channel-ovr.md): uma subdivisão de uma linha. O conhecimento dos canais normalmente não é necessário para um aplicativo porque o provedor de serviços configura como eles serão exibidos como endereços.
-   [Endereço](address-ovr.md): um local de rede em uma rede. Cada linha ou canal tem um ou mais endereços associados. O endereço é um conceito-chave tanto no TAPI 3,1 (TAPI/COM) quanto na TAPI 2,2 (TAPI/C).
-   [Terminal](terminal-ovr.md): uma fonte ou um renderizador para um endereço e tipo de mídia específicos.

Os provedores de serviço relatam as características do dispositivo à TAPI em resposta às consultas do aplicativo. Provedores de serviço também iniciam relatórios sobre alterações no estado do dispositivo. Essas alterações são relatadas para um aplicativo com base nas notificações solicitadas durante a inicialização.

As características básicas do dispositivo são:

-   [Classe de dispositivo](device-class-ovr.md)
-   [Identificador do dispositivo](device-identifier-ovr.md)
-   [Tipo de endereço](address-type-ovr.md)
-   [Identificador de endereço](address-identifier-ovr.md)
-   [Eventos de dispositivo](device-events-ovr.md)
-   [Tipo de mídia](media-type-ovr.md)
-   [Tipo de terminal](terminal-type-ovr.md)

Além disso, os provedores de serviço fornecem informações relacionadas à capacidade de um determinado endereço para executar várias operações de sessão.

As características complementares podem ser associadas a determinados dispositivos, se os provedores de serviços oferecerem suporte a eles. Um aplicativo TAPI 2. x descobre recursos usando as funções [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) . Os aplicativos TAPI 3. x usam a interface [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) para essa finalidade.

A TAPI 2. x fornece um conjunto especial de operações complementares que o provedor de serviços pode implementar para uso com dispositivos de telefone. Consulte [dispositivos de telefone](./opening-and-closing-phone-devices.md).

Recursos estendidos são específicos do provedor e não são diretamente cobertos pela API de telefonia da Microsoft. Consulte [funções de linha estendidas](./extended-line-functions.md), [funções de telefone de telefonia estendidas](./extended-telephony-phone-functions.md)ou [interfaces específicas de provedor](provider-specific-interfaces.md).

Abaixo está um resumo das operações TAPI que consultam os provedores de serviço nas características do dispositivo e fornecem dados sobre o estado atual.



| Funções TAPI 2. x                                                  | Descrição                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Consulta um dispositivo de linha especificado para determinar os recursos de telefonia dos endereços associados.               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Consulta um dispositivo de linha especificado para determinar os recursos de telefonia do endereço específico.                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Retorna uma estrutura de dados "opaca" que armazena a configuração atual de um dispositivo.                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Restaura a configuração do dispositivo.                                                                                 |
| [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Exibe uma caixa de diálogo que permite ao usuário configurar parâmetros relacionados ao dispositivo.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Recupera um identificador de dispositivo estável que pode ser usado em chamadas de função TAPI adicionais ou com uma API diferente. |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Consulta o status atual do dispositivo, como o número de chamadas ativas.                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Define o status do dispositivo, como a definição de um dispositivo como não em serviço.                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Recupera o ícone específico do provedor para exibição para o usuário.                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Permite que um aplicativo negocie uma versão de extensão para usar com o dispositivo de linha especificado.                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Fornece acesso a recursos específicos do dispositivo.                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Envia recursos específicos do dispositivo para o provedor de serviços.                                                        |



 



| Interfaces ou métodos TAPI 3. x                                   | Descrição                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Obtém informações sobre os recursos de um endereço.                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Define e Obtém o formato de mídia do™ do DirectShow.                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Define e obtém características de terminal de áudio padrão, como volume.                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Obtém informações sobre os recursos de suporte de mídia de um endereço.                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Interface base para o objeto terminal. Obtém informações como a classe de terminal e a mídia com suporte. |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Obtém informações sobre terminais disponíveis e cria terminais adicionais.                               |
| [Interfaces específicas do provedor](provider-specific-interfaces.md) | Dependente do provedor de serviços.                                                                             |



 

 

 
