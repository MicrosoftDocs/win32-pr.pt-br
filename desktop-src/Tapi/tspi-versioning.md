---
description: Saiba mais sobre o controle de versão do TSPI. Com o tempo, versões diferentes de TAPI, aplicativos e provedores de serviços podem ser produzidos.
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: Controle de versão do TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989231"
---
# <a name="tspi-versioning"></a>Controle de versão do TSPI

Com o tempo, versões diferentes de TAPI, aplicativos e provedores de serviços podem ser produzidos. Essas novas versões podem fazer novas definições, como para novos recursos, novos membros em estruturas de dados e novos campos de bits. Portanto, os números de versão são necessários para indicar como interpretar várias estruturas de dados.

Para permitir a interoperabilidade ideal de diferentes versões de aplicativos, versões da própria TAPI e versões de provedores de serviço por diferentes fornecedores, a telefonia da Microsoft fornece um mecanismo de negociação de versão simples para aplicativos. Há duas versões diferentes que precisam ser acordadas pela TAPI e pelo provedor de serviços de telefonia para cada dispositivo de linha. O primeiro é o número de versão para o SPI de telefonia básico e suplementar, chamado de versão da *interface TSPI*. O outro é para extensões específicas do provedor, se houver, e é chamado de versão de *extensão*. O formato das estruturas e dos tipos de dados usados pelos recursos básicos e complementares do TSPI é definido pela versão do TSPI, enquanto a versão da extensão determina o formato das estruturas de dados definidas pelas extensões específicas do fornecedor.

Esses dois tipos de negociação de versão são tratados por dois procedimentos diferentes: [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) é usado para negociar a versão da interface TSPI e [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) é usado para negociar a versão da extensão. A negociação de versão de extensão poderá ser ignorada se as extensões não forem desejadas. Se esses intervalos forem inseridos durante a sobreposição de negociação, o provedor de serviços deverá retornar um valor dentro da parte sobreposta do intervalo como o resultado da negociação. Normalmente, isso deve ser o maior valor possível. Se os intervalos não se sobrepõem, as duas partes são incompatíveis e a função retorna um erro.

Os resultados de uma negociação simplesmente indicam que o provedor de serviços está disposto a operar em um determinado número de versão, mas não confirma o provedor de serviços para fazê-lo. Por exemplo, a TAPI pode ser renegociada para determinar uma versão ideal depois de ter negociado uma versão possível. A versão da interface TSPI só é confirmada quando uma linha é aberta usando [**\_ lineOpen TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) e sobreviver até que o dispositivo seja fechado. A versão de extensão é confirmada quando a função [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) é chamada e sobreviver até que a seleção seja cancelada selecionando a versão de extensão zero.

A seleção de versão de extensão pode ocorrer muitas vezes, incluindo enquanto uma versão de extensão está em vigor. Como o provedor de serviços está comprometido com a versão de extensão, seu intervalo de versões com suporte limita exatamente essa versão de extensão. Por exemplo, considere um provedor de serviços que normalmente é compatível com as versões de extensão 1,0 a 5,5. Se a versão 3,0 estiver em vigor enquanto um chamador tentar negociar uma versão dentro do intervalo de 1,0 a 5,5, a negociação retornará 3,0.

Como a TAPI negocia a versão, você pode atualizar um provedor de serviços para novas versões da interface sem exigir que a TAPI também seja atualizada. Da mesma forma, a TAPI pode ser atualizada e ainda usar o provedor de serviços mais antigo.

 

 
