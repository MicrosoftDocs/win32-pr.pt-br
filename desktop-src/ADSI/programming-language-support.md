---
title: Suporte à linguagem de programação
description: Você pode escrever aplicativos cliente ADSI em vários idiomas.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe355e3274821bf81a666380bfe70ca0f3f7b49e2bc9de10bf2aa4796b5288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023294"
---
# <a name="programming-language-support"></a>Suporte à linguagem de programação

Você pode escrever aplicativos cliente ADSI em vários idiomas. Para a maioria das tarefas administrativas, a ADSI define interfaces e objetos acessíveis de linguagens compatíveis com a Automação. Por exemplo, o sistema de desenvolvimento do Microsoft Visual Basic, o Microsoft Visual Basic Scripting Edition (VBScript) e o Java, bem como mais linguagens de desempenho e eficiência, como C e C++.

A integração suave com Active Server Pages e VBScript facilitam a gravação de aplicativos da Internet que acessam serviços de diretório. Para integração com OLE DB, a ADSI fornece um provedor OLE DB, dando suporte a um subconjunto das interfaces de OLE DB de consulta. O OLE DB provedor dá suporte ao acesso somente leitura ao Active Directory.

Para aplicativos de Internet, o uso de scripts em arquivos ASP (página Active Server) pode criar e manipular objetos ADSI no servidor e exibir os resultados em uma página da Web. No Console de Gerenciamento Microsoft, os snap-ins de administração de serviço de diretório podem usar a ADSI para encontrar serviços de diretório de interesse. Em resumo, as Interfaces de Serviço do Active Directory podem fornecer acesso a um amplo e diversificado conjunto de serviços de diretório , incluindo aqueles que ainda não foram construídos.

Para acesso a estruturas que usam APIs tradicionais, a arquitetura ADSI define interfaces de baixo nível que não são suportadas pela Automação que podem ser acessadas em linguagens como C e C++. Essas interfaces são pouco mais do que wrappers COM para protocolos de rede para um serviço de diretório.

Escrever código nas interfaces publicadas permite que seu aplicativo alcance os serviços de diretório para todos os provedores ADSI instalados e integre os dados resultantes. Com pouca ou nenhuma alteração no código, seu aplicativo pode continuar acessando serviços de diretório adicionais em sua rede à medida que novos provedores ADSI são instalados.

A figura a seguir mostra como a ADSI se encaixa em um ambiente de aplicativo. Se o aplicativo for escrito em Visual Basic, C/C++, VBScript, sistema de desenvolvimento do Microsoft JScript ou como um aplicativo Web usando páginas do Active Server, as Interfaces de Serviço do Active Directory fornecem um acesso limpo e fácil de usar aos serviços de diretório subjacentes sem a necessidade de usar as APIs de rede nativas.

![Suporte adsi para linguagens de programação](images/ds2layr.png)

Conforme mostrado na figura anterior, os clientes que não são suportados pela Automação têm acesso a todas as interfaces ADSI, incluindo interfaces COM puras com a convenção de nomenal **IDirectoryXXX** e interfaces COM de Automação com a convenção de **nomenal IADsXXX**. Como os clientes solicitam predominantemente informações dos serviços de diretório, o modelo de consulta flexível ADSI por meio de OLE DB [**e IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) é eficaz.

 

 




