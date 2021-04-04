---
title: Associação a um objeto Active Directory
description: A maneira mais comum de associar a um objeto de Active Directory é usar a função GetObject entre um cliente ADSI e um provedor ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Ligando a um objeto Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59992dbc88c00be6306dec24523ec4e030d4a516
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823980"
---
# <a name="binding-to-an-active-directory-object"></a>Associação a um objeto Active Directory

A maneira mais comum de associar a um objeto de Active Directory é usar a função **GetObject** entre um cliente ADSI e um provedor ADSI. Essa também é a maneira mais fácil de mostrar como o componente de provedor recebe e serviços de solicitações. Tanto a função ADSI API [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) quanto a função Visual Basic **GetObject** seguem as mesmas etapas para associação.

Para este exemplo, suponha que o cliente ADSI é um aplicativo de visualizador ADSI que recebeu o ADsPath "Sample://Seattle/Redmond/Shelly" da interface do usuário (1). A figura a seguir detalha a sequência de eventos numerando as setas de fluxo.

![exibição detalhada dos componentes ADSI](images/dscsex.png)

Na figura anterior, o cliente inicia a solicitação para um ponteiro de interface no objeto Active Directory representado pelo ADsPath "Sample://Seattle/Redmond/Shelly" dos serviços ADSI (2). Durante a inicialização, o software de serviços populava uma tabela de identificadores programáticos do provedor instalado (ProgIDs) a partir do registro ("LDAP:", "exemplo:", "WinNT:" e assim por diante) e os emparelharam com os s **CLSID** correspondentes que identificam o módulo de software apropriado.

O servidor ADSI verifica se o ProgID, neste caso, "Sample:", existe no ADsPath. Em seguida, ele cria um contexto de associação para otimizar referências adicionais a esse objeto e chama a função COM padrão [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) para criar um moniker com que pode ser usado para localizar e associar ao objeto que representa o usuário "Shelly".

Na seção a seguir, os nomes de arquivo do componente do provedor de exemplo código-fonte são incluídos entre parênteses, quando apropriado.

Como em outras implementações de servidor COM, o [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) examina o ProgID e pesquisa o **CLSID** apropriado no registro (3) para localizar o código de fábrica de classe fornecido pelo provedor correspondente (Cprovcf. cpp) na implementação do provedor apropriado (4). Esse código cria um objeto inicial de nível superior que implementa o método [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov. cpp). A implementação do provedor de **ParseDisplayName** resolve o caminho no próprio namespace do provedor. Isso eventualmente chama ADsObject e invoca o analisador fornecido com o componente do provedor (Parse. cpp) para verificar se o ADsPath está sintaticamente correto para esse namespace.

**GetObject**, que é definido em Getobj. cpp, determina se o objeto solicitado é um objeto de namespace, um objeto de esquema ou algum outro tipo de objeto. Se um dos dois primeiros, esse tipo de objeto de classe de esquema é criado e o ponteiro de interface apropriado é recuperado. Caso contrário, o caminho do diretório de exemplo será criado a partir do ADsPath (por exemplo, " \\ Seattle \\ Redmond \\ Shelly", mas em um serviço de diretório diferente, talvez tenha tido que " \\ ou = Seattle \\ ou = Redmond \\ CN = Shelly") e o controle passe para SampleDSOpenObject, o que abre o objeto no armazenamento de dados de exemplo e também recupera seu tipo de objeto (neste caso, "User

Com os dados coletados, um novo objeto é criado (6) para representar o item descrito pelo ADsPath, e um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nesse objeto é recuperado. Nesse caso, é criado um objeto Active Directory genérico que dá suporte aos métodos **IUnknown** e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj. cpp, Core. cpp). A rotina CSampleDSGenObject:: AllocateGenObject lê os dados da biblioteca de tipos para criar as entradas de expedição adequadas para esses novos objetos a fim de oferecer suporte a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

O encapsulamento deste ponteiro de interface em um moniker conclui a função ResolvePathName (Cprov. cpp) e analisa o nome de exibição.

Todos os objetos COM criados durante esse processo são armazenados em cache por motivos de desempenho e gerenciados por meio do contexto de associação. Isso melhora o desempenho para outras operações no mesmo objeto que segue imediatamente a associação de moniker.

Esse objeto de Active Directory bem formado agora é consultado para o identificador de interface solicitado para a chamada [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) inicial e um ponteiro para essa interface é recuperado (7) e passado de volta pelo servidor ADSI para o cliente (8&9). A partir desse caso, o cliente funciona diretamente com o componente do provedor por meio dos métodos de interface até que a solicitação inicial seja satisfeita (10).

Além disso, as solicitações de dados de objeto do cliente geralmente assumem a forma de solicitações de gets e takes de propriedade, todas otimizadas por meio da implementação do provedor de um cache de propriedade (cProps. cpp). Empacotar e desempacotar dados de forma inteligente, muitas vezes incluindo copiar e liberar estruturas e cadeias de caracteres, entre os tipos de dados nativos no sistema operacional do componente de provedor de exemplo e o tipo de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) de automação com suporte pelo ADSI ocorre antes que as propriedades sejam carregadas no cache (Smpoper. cpp).

O componente de provedor de exemplo é projetado de forma que as chamadas reais para o sistema operacional sejam logicamente isoladas do componente do provedor, criando software portátil para mais de um sistema operacional (RegDSAPI. cpp).

 

 