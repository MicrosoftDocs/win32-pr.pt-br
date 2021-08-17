---
description: Saiba mais sobre o versionamento de TSPI. Ao longo do tempo, diferentes versões da TAPI, aplicativos e provedores de serviços podem ser produzidas.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Versão do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee1e1d77a33861c7943c8bda063432cd5f212971adae88ef8bdd1eb2c4f88a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944303"
---
# <a name="tspi-versioning"></a>Versão do TSPI

Ao longo do tempo, diferentes versões da TAPI, aplicativos e provedores de serviços podem ser produzidas. Essas novas versões podem fazer novas definições, como para novos recursos, novos membros em estruturas de dados e novos campos de bits. Portanto, os números de versão são necessários para indicar como interpretar várias estruturas de dados.

Para permitir a interoperabilidade ideal de diferentes versões de aplicativos, versões da PRÓPRIA TAPI e versões de provedores de serviços por fornecedores diferentes, a Telefonia da Microsoft fornece um mecanismo de negociação de versão simples para aplicativos. Há duas versões diferentes que precisam ser aceitas pela TAPI e pelo provedor de serviços de telefonia para cada dispositivo de linha. O primeiro é o número de versão para a SPI de Telefonia Básica e Suplementar, conhecida como a versão da *interface TSPI*. A outra é para extensões específicas do provedor, se alguma, e é conhecida como a versão *de extensão*. O formato das estruturas de dados e tipos de dados usados pelos recursos Básico e Suplementar do TSPI é definido pela versão do TSPI, enquanto a versão da extensão determina o formato das estruturas de dados definidas pelas extensões específicas do fornecedor.

Esses dois tipos de negociação de versão são tratados por dois procedimentos diferentes: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) é usado para negociar a versão da interface TSPI e [**tSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) é usado para negociar a versão da extensão. A negociação de versão da extensão pode ser ignorada se as extensões não são procuradas. Se esses intervalos de entrada durante a negociação se sobrepõem, o provedor de serviços deve retornar um valor dentro da parte sobreposta do intervalo como resultado da negociação. Normalmente, esse deve ser o valor mais alto possível. Se os intervalos não se sobrepõem, as duas partes são incompatíveis e a função retorna um erro.

Os resultados de uma negociação simplesmente indicam que o provedor de serviços está disposto a operar em um número de versão específico, mas não confirma o provedor de serviços para fazer isso. Por exemplo, a TAPI pode negociar para determinar uma versão ideal depois de ter negociado uma versão possível. A versão da interface TSPI só é confirmado quando uma linha é aberta usando [**\_ lineOpen TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e sobrevive até que o dispositivo seja fechado. A versão da extensão é confirmada quando a função [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) é chamada e sobrevive até que a seleção seja cancelada selecionando a extensão versão zero.

A seleção de versão da extensão pode ocorrer muitas vezes, incluindo enquanto uma versão de extensão está em vigor. Como o provedor de serviços está comprometido com a versão da extensão, seu intervalo de versões com suporte é limitado exatamente a essa versão de extensão. Por exemplo, considere um provedor de serviços normalmente compatível com as versões de extensão 1.0 a 5.5. Se a versão 3.0 estiver em vigor enquanto um chamador tentar negociar uma versão dentro do intervalo de 1.0 a 5.5, a negociação retornará 3.0.

Como a TAPI negocia a versão, você pode atualizar um provedor de serviços para novas versões da interface sem exigir que a TAPI também seja atualizada. Da mesma forma, a TAPI pode ser atualizada, mas ainda usar seu provedor de serviços mais antigo.

 

 
