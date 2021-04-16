---
description: Com o tempo, podem existir versões diferentes para TAPI, aplicativos e provedores de serviços para uma linha ou telefone.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Negociação de versão TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f41f4ca6f12862d6fc19f982c48b90bdafe2aaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779441"
---
# <a name="tapi-version-negotiation"></a>Negociação de versão TAPI

Com o tempo, podem existir versões diferentes para TAPI, aplicativos e provedores de serviços para uma linha ou telefone. Novas versões podem definir novos recursos, novos campos para estruturas de dados e assim por diante. Portanto, os números de versão indicam como interpretar várias estruturas de dados.

Para permitir a interoperabilidade ideal de diferentes versões de aplicativos, versões da própria TAPI e versões de provedores de serviço por diferentes fornecedores, a TAPI fornece um mecanismo de negociação de versão simples e em duas etapas para aplicativos. Duas versões diferentes devem ser acordadas pelo aplicativo, pela TAPI e pelo provedor de serviços para cada dispositivo de linha. O primeiro é o número de versão para telefonia básica e suplementar e é conhecido como a versão da API. O outro é para extensões específicas do provedor, se houver, e é chamado de versão de extensão. O formato das estruturas e dos tipos de dados usados pelos recursos básicos e complementares da TAPI é definido pela versão da API, enquanto a versão da extensão determina o formato das estruturas de dados definidas pelas extensões específicas do fornecedor.

A negociação de versão prossegue em duas fases. Na primeira fase, o número de versão da API é negociado e o identificador de extensão associado a todas as extensões específicas do fornecedor com suporte no dispositivo é obtido. Na segunda fase, a versão da extensão é negociada. Se o aplicativo não usar nenhuma extensão de API, ele ignorará a segunda fase e as extensões não serão ativadas pelo provedor de serviços. Se o aplicativo quiser usar extensões, mas as extensões do provedor de serviços (o identificador de extensão) não forem reconhecidas pelo aplicativo, o aplicativo também deverá ignorar a negociação para a versão de extensão. Cada fornecedor tem seu próprio conjunto de versões legais (reconhecidas) para cada conjunto de especificações de extensão que distribui.

A função [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) é usada para negociar o número de versão da API a ser usado. Ele também recupera o identificador de extensão suportado pelo dispositivo de linha, retornando zeros se nenhuma extensão tiver suporte. Com essa chamada de função, o aplicativo fornece o intervalo de versão da API com o qual ele é compatível. A TAPI, por sua vez, negocia com o provedor de serviços da linha para determinar a qual intervalo de versão da API ele dá suporte. A TAPI seguinte seleciona um número de versão (normalmente, embora não necessariamente, o número de versão mais alto) no intervalo de versões sobrepostas que o aplicativo, a DLL e o provedor de serviços forneceu. Esse número é retornado para o aplicativo, junto com o identificador de extensão que define as extensões disponíveis do provedor de serviços da linha.

Se o aplicativo quiser usar as extensões definidas pelo identificador de extensão retornado, ele deverá primeiro chamar [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) para negociar a versão de extensão. Em uma fase de negociação semelhante, o aplicativo especifica a versão de API já acordada e o intervalo de versão de extensão com suporte. A TAPI passa essas informações para o provedor de serviços para a linha. O provedor de serviços verifica a versão da API e o intervalo de versão da extensão em relação a sua própria e seleciona o número de versão da extensão apropriado, se houver.

Quando o aplicativo chama [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)posteriormente, ele retorna um conjunto de recursos de dispositivo para a linha que corresponde aos resultados da negociação de versão. Isso inclui os recursos de dispositivo da linha consistentes com a versão da API e os recursos específicos do dispositivo da linha consistentes com a versão da extensão. O aplicativo deve especificar ambos os números de versão ao abrir uma linha. Nesse ponto, o aplicativo, a DLL e o provedor de serviços estão comprometidos a usar as versões acordadas. Se as extensões específicas do dispositivo não forem usadas, a versão da extensão deverá ser especificada como zero.

Em um ambiente em que vários aplicativos abrem o mesmo dispositivo de linha, o primeiro aplicativo para abrir o dispositivo de linha seleciona as versões de todos os aplicativos futuros que desejam usar a linha (os provedores de serviço não oferecem suporte a várias versões simultaneamente). Da mesma forma, um aplicativo que abre vários dispositivos de linha pode achar mais fácil operar todos os dispositivos de linha sob o mesmo número de versão da API.

Cada função que usa um parâmetro *dwAPIVersion* ou semelhante deve definir esse parâmetro como a versão de API mais alta com suporte do aplicativo ou a versão de API negociada usando a função [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) ou [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) em um dispositivo específico. Use a tabela a seguir como guia:



| Função                                                     | Significado                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Use a versão retornada por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Use a versão mais recente com suporte do aplicativo.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Use a versão retornada por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Use a versão mais recente com suporte do aplicativo.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Use a versão mais recente com suporte do aplicativo.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Use a versão mais recente com suporte do aplicativo.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Use a versão retornada por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Use a versão retornada por [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Use a versão mais recente com suporte do aplicativo.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Use a versão mais recente com suporte do aplicativo.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Use a versão retornada por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Use a versão mais recente com suporte do aplicativo.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Use a versão retornada por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Use a versão retornada por [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Ao negociar uma versão de API, sempre defina os números de versão alta e baixa para o intervalo de versões para as quais seu aplicativo pode dar suporte. Por exemplo, nunca use 0x00000000 para a versão baixa ou 0xFFFFFFFF para a alta porque esses valores exigem que seu aplicativo dê suporte a todas as versões da TAPI, no passado e no futuro.

 

 

 



