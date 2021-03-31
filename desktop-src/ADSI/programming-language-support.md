---
title: Suporte à linguagem de programação
description: Você pode escrever aplicativos cliente ADSI em vários idiomas.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822192"
---
# <a name="programming-language-support"></a>Suporte à linguagem de programação

Você pode escrever aplicativos cliente ADSI em vários idiomas. Para a maioria das tarefas administrativas, a ADSI define interfaces e objetos acessíveis de linguagens em conformidade com a automação. Por exemplo, o sistema de desenvolvimento da Microsoft Visual Basic, o Microsoft Visual Basic Scripting Edition (VBScript) e o Java, bem como mais linguagens de desempenho e eficiência, como C e C++.

A integração tranqüila com as páginas Active Server e o VBScript facilita a gravação de aplicativos de Internet que acessam os serviços de diretório. Para a integração com OLE DB aplicativos, a ADSI fornece um provedor de OLE DB ao oferecer suporte a um subconjunto das interfaces de consulta OLE DB. O provedor de OLE DB dá suporte ao acesso somente leitura ao Active Directory.

Para aplicativos da Internet, o uso de scripts em arquivos ASP (página de Active Server) pode criar e manipular objetos ADSI no servidor e exibir os resultados em uma página da Web. No console de gerenciamento Microsoft, os snap-ins de administração do serviço de diretório podem usar ADSI para localizar serviços de diretório de interesse. Em suma, Active Directory interfaces de serviço podem fornecer acesso a um conjunto amplo e diversificado de serviços de diretório, incluindo aqueles ainda não compilados.

Para acessar estruturas que usam APIs tradicionais, a arquitetura ADSI define interfaces de baixo nível que não dão suporte à automação que são acessíveis de linguagens como C e C++. Essas interfaces são pouco mais do que wrappers COM para protocolos de rede para um serviço de diretório.

Escrever código para as interfaces publicadas permite que seu aplicativo alcance serviços de diretório para todos os provedores ADSI instalados e integre os dados resultantes. Com pouca ou nenhuma alteração no seu código, seu aplicativo pode continuar a acessar serviços de diretório adicionais na sua rede à medida que novos provedores ADSI são instalados.

A figura a seguir mostra como o ADSI se encaixa em um ambiente de aplicativo. Quer o aplicativo seja escrito em Visual Basic, C/C++, VBScript, Microsoft JScript Development System ou como um aplicativo Web usando Active Server páginas, Active Directory interfaces de serviço fornecem um acesso limpo e fácil de usar aos serviços de diretório subjacentes sem precisar usar as APIs de rede nativas.

![suporte ADSI para linguagens de programação](images/ds2layr.png)

Conforme mostrado na figura anterior, os clientes que não dão suporte à automação têm acesso a todas as interfaces ADSI, incluindo interfaces COM puras com a Convenção de nomenclatura **IDirectoryXXX** e interfaces com de automação com a Convenção de nomenclatura **IADsXXX**. Como os clientes solicitam predominantemente informações de serviços de diretório, o modelo de consulta flexível da ADSI por meio de OLE DB e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) é eficaz.

 

 




