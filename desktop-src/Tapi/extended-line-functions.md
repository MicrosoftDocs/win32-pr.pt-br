---
description: Os serviços de linha estendida (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviços para a API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funções de linha estendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394ad011a5752a45f82de4934a3f87c9f1590870b245fdc113f57badb4298290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003654"
---
# <a name="extended-line-functions"></a>Funções de linha estendida

Os serviços de linha estendida (ou serviços de linha específicos do dispositivo) incluem todas as extensões definidas pelo provedor de serviços para a API. A API define um mecanismo que permite que os fornecedores do provedor de serviços estendam a TAPI usando extensões específicas do dispositivo. A API define apenas o mecanismo de extensão e, ao fazer isso, fornece acesso a extensões específicas do dispositivo, mas a API não define seu comportamento. O comportamento é completamente definido pelo provedor de serviços.

A TAPI consiste em definições de constante escalar e bit-flag, estruturas de dados, funções e mensagens. Os procedimentos são definidos que permitem que um fornecedor estenda a maioria deles da seguinte maneira.

Para constantes de dados escalares extensíveis, um fornecedor de provedor de serviços pode definir novos valores em um intervalo especificado. Como a maioria das constantes de dados são **DWORDs,** normalmente, o intervalo entre 0x00000000 e 0x7FFFFFFF é reservado para extensões futuras comuns, enquanto 0x80000000 por meio de 0xFFFFFFFF estão disponíveis para extensões específicas do fornecedor. A suposição é que um fornecedor definiria valores que são extensões naturais dos tipos de dados definidos pela API.

Para constantes de dados de sinalizador de bits extensíveis, um fornecedor do provedor de serviços pode definir novos valores para bits especificados. Como a maioria das constantes de sinalizador de bits são **DWORDs,** normalmente um número específico dos bits inferiores é reservado para extensões comuns, enquanto os bits superiores restantes estão disponíveis para extensões específicas do fornecedor. Sinalizadores de bits comuns são atribuídos do bit zero para cima; Extensões específicas do fornecedor devem ser atribuídas do bit 31 para baixo. Isso fornece máxima flexibilidade na atribuição de posições de bit a extensões comuns versus extensões específicas do fornecedor. Espera-se que um fornecedor defina novos valores que são extensões naturais dos sinalizadores de bits definidos pela API.

Estruturas de dados extensíveis têm um campo de tamanho variavel reservado para uso específico do dispositivo. Sendo dimensionado de forma variavel, o provedor de serviços decide a quantidade de informações e a interpretação. Espera-se que um fornecedor que define um campo específico do dispositivo faça essas extensões naturais da estrutura de dados original definida pela API.

Duas funções, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) e [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)e duas mensagens relacionadas, [**LINE \_ DEVSPECIFIC**](line-devspecific.md) e [**LINE \_ DEVSPECIFICFEATURE,**](line-devspecificfeature.md)fornecem um mecanismo de extensão específico do fornecedor. A **função lineDevSpecific** e a mensagem LINE DEVSPECIFIC associada permitem que um aplicativo acesse recursos de linha, endereço ou chamada específicos do dispositivo que não estão disponíveis com os serviços de Telefonia Básica ou \_ Suplementar. O perfil de parâmetro da **função lineDevSpecific** é genérico nessa pequena interpretação dos parâmetros feita pela API. A interpretação dos parâmetros é definida pelo provedor de serviços e deve ser compreendida por um aplicativo que os usa. Os parâmetros são simplesmente passados pelo TAPI do aplicativo para o provedor de serviços. Um aplicativo que depende de extensões específicas do dispositivo geralmente não funcionará com outros provedores de serviços; no entanto, os aplicativos gravados nos serviços básico e de telefonia suplementar funcionarão com o provedor de serviços estendidos.

Para sua conveniência, uma função de escape mais especializada também é fornecida. Ele é semelhante a [**lineDevSpecific,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)mas coloca a interpretação em alguns dos parâmetros. Essa função mais especializada é [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), uma função de escape específica do dispositivo para permitir o envio de recursos de opção para a opção. A mensagem [**LINE \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) é a mensagem específica do dispositivo enviada ao aplicativo como uma indicação dos recursos enviados para a opção. Essa função e sua mensagem associada permitem que um aplicativo emular pressiona o botão no telefone de recurso da linha. Como os telefones de recurso e os significados de seus botões são específicos do fornecedor, a invocação de recursos usando [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) também é específica do fornecedor.

Conforme mencionado anteriormente, não há registro central para identificadores de fabricante. Em vez disso, um gerador de identificador exclusivo (EXTIDGEN) é disponibilizado.

 

 



