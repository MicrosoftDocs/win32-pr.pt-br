---
description: O MUI permite que seus aplicativos gerenciem idiomas da interface do usuário de duas maneiras.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Gerenciamento de idioma da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370783"
---
# <a name="user-interface-language-management"></a>Gerenciamento de idioma da interface do usuário

O MUI permite que seus aplicativos gerenciem idiomas da interface do usuário de duas maneiras. Um aplicativo pode usar uma abordagem simples para o gerenciamento de linguagem, padronizando para as configurações de idioma do sistema operacional. Como alternativa, o aplicativo pode dar suporte a seus próprios idiomas dos quais o usuário pode selecionar. A API do MUI também permite que seu aplicativo acesse diretamente as linguagens e as listas de idiomas com suporte no sistema operacional e mantidas pelo carregador de recursos. O restante deste tópico define os idiomas com suporte do sistema e o mecanismo de fallback de idioma.

## <a name="languages-maintained-by-the-operating-system"></a>Idiomas mantidos pelo sistema operacional

### <a name="system-default-ui-languageinstall-language"></a>Idioma da interface do usuário padrão do sistema/idioma de instalação

O idioma da interface do usuário padrão do sistema é o idioma da versão localizada usada para configurar o Windows. Todos os menus, caixas de diálogo, mensagens de erro e arquivos de ajuda são representados nesse idioma, exceto quando o usuário seleciona um idioma diferente.

No Windows Vista e posterior, o idioma da interface do usuário padrão do sistema é conhecido como "idioma de instalação" e desempenha uma função mais limitada. Para a maioria dos fins, ele é substituído pelos idiomas de interface do usuário preferenciais do sistema. No entanto, em determinados contextos, é útil ter uma única linguagem de instalação que é sempre conhecida como totalmente suportada.

Nenhuma função MUI está disponível para definir o idioma da interface do usuário padrão do sistema. Para recuperar esse idioma, o aplicativo pode chamar [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Idioma da interface do usuário do sistema

O sistema operacional define o idioma da interface do usuário do sistema como um idioma de interface de usuários que pode ser definido por um administrador na guia **avançado** da parte de opções regionais e de idiomas do painel de controle. O sistema operacional usará esse idioma se o usuário atual não tiver feito configurações de idioma específicas ou se nenhuma conta ativa estiver conectada. O idioma só poderá ser alterado se mais de um idioma da interface do usuário estiver instalado no computador.

> [!Note]  
> O sistema operacional deve ser reinicializado para todos os usuários e serviços para ver o efeito da alteração de idioma.

 

Nenhuma função MUI está disponível para definir o idioma da interface do usuário do sistema. Para recuperar esse valor, um aplicativo direcionado ao Windows Vista e posterior pode chamar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e obter o primeiro idioma na lista de idiomas da interface do usuário preferencial do sistema. Os aplicativos destinados a sistemas operacionais anteriores ao Windows Vista não podem usar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e devem ser baseados na suposição de que o idioma da interface do usuário do sistema sempre é o mesmo que o idioma da interface do usuário padrão do sistema.

### <a name="user-ui-language"></a>Idioma da interface do usuário

O idioma da interface do usuário determina o idioma da interface do usuário usado para menus, caixas de diálogo, arquivos de ajuda e assim por diante. Ele pode ser definido pelo usuário atual na guia **idioma** da parte de opções regionais e de idioma do painel de controle. Esse idioma só poderá ser alterado se mais de um idioma da interface do usuário estiver instalado no computador. Observe que o usuário precisará fazer logoff e, em seguida, fazer logon novamente para ver o efeito. Por exemplo, uma empresa multinacional deseja implantar o Windows em todas as suas subsidiárias. A empresa cria um trabalho de instalação global, que instala a versão de idioma inglês do Windows em todos os clientes, independentemente do local. Ao mesmo tempo, ele instala módulos de idioma específicos dependendo da unidade organizacional da qual um computador é membro. Quando o usuário faz logon pela primeira vez em um sistema operacional recentemente instalado, o Windows aparece como uma versão localizada.

No Windows Vista e versões posteriores, o idioma da interface do usuário é o primeiro idioma na lista de idiomas da interface do usuário preferencial. Observe que os idiomas de fallback podem ser usados se recursos específicos não estiverem disponíveis neste idioma.

Em sistemas operacionais anteriores ao Windows Vista, o idioma da interface do usuário é geralmente o mesmo que o idioma da interface de usuário padrão do sistema. No entanto, para o MUI do Windows, os dois idiomas podem ser diferentes.

Para recuperar o idioma da interface do usuário, um aplicativo pode chamar [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) ou [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages). O aplicativo não pode alterar o idioma da interface do usuário, pois não há nenhuma função para defini-lo.

## <a name="language-lists-maintained-by-the-operating-system"></a>Listas de idiomas mantidas pelo sistema operacional

### <a name="system-preferred-ui-languages-list"></a>Lista de idiomas da interface do usuário preferencial do sistema

O carregador de recursos mantém uma lista de idiomas de interface do usuário preferencial do sistema. Estão incluídos nessa lista os idiomas preferenciais pelo sistema operacional para seus próprios recursos, como menus e caixas de diálogo, mensagens, arquivos INF e arquivos de ajuda. A lista é composta pelo idioma da interface do usuário padrão do sistema e pelo idioma da interface do usuário do sistema e seus fallbacks. Um aplicativo pode recuperar idiomas da interface do usuário preferenciais do sistema chamando [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages).

### <a name="user-preferred-ui-languages-list"></a>Lista de idiomas de interface do usuário preferenciais

O carregador de recursos usa uma lista de idiomas de interface de usuário preferencial do usuário que inclui os idiomas que o usuário prefere. O carregador de recursos usa os recursos que correspondem aos idiomas dessa lista, se disponível, para um thread de aplicativo específico. Essas linguagens têm precedência sobre as preferências do sistema. Para recuperar idiomas de interface do usuário preferenciais, seu aplicativo pode chamar [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Processar lista de idiomas da interface do usuário preferencial

No Windows Vista e posterior, o carregador de recursos mantém uma lista de idiomas de interface do usuário preferencial do processo que consiste em até cinco idiomas válidos definidos por um processo em execução para um aplicativo MUI. Os idiomas podem ser definidos pelo aplicativo com uma chamada para [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). O aplicativo pode recuperar os idiomas chamando [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Lista de idiomas da interface do usuário preferencial de thread

No Windows Vista e posterior, o carregador de recursos usa uma lista de idiomas de interface do usuário preferencial de thread que consiste em até cinco idiomas válidos definidos por um thread em um processo em execução para um aplicativo MUI. Esses idiomas são usados para personalizar os idiomas da interface do usuário do aplicativo e torná-los diferentes do idioma do sistema operacional. A lista de idiomas da interface do usuário preferencial do thread é baseada nos idiomas da interface do usuário preferenciais do sistema, nos idiomas de interface de usuário preferenciais e no idioma padrão da interface do usuário.

Para definir os idiomas de interface do usuário preferenciais do thread, o aplicativo deve chamar [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Para recuperar esses idiomas, o aplicativo chama [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Representação de linguagem neutra

Uma linguagem neutra é representada apenas como a linguagem, sem região ou localidade. Por exemplo, a representação neutra do idioma Inglês (Canadá), en-CA, é representada como "en". Embora uma linguagem neutra não esteja associada aos aspectos de uma região ou localidade, você pode associá-la a um conjunto de recursos. Normalmente, um recurso de idioma neutro é baseado no uso na região mais predominante para a linguagem.

Como ilustração, suponha que seu aplicativo MUI Localize os recursos do idioma alemão para alemão (Suíça) representado como de-CH e alemão (Áustria) representado como de um, ao mesmo tempo em que cria um conjunto completo de recursos para alemão (Alemanha) representado como de-DE. Você deve tomar decisões para este aplicativo considerando arquivos de recursos inteiros. Se o aplicativo duplicar os recursos de de-DE como recursos de idioma neutro, ele deverá fornecer um idioma de fallback para o carregador de recursos. Se o carregador não encontrar um determinado arquivo de recursos específico de idioma para de-CH ou para de, ele voltará para os recursos "de" de idioma neutro. Esses recursos são mais bem mais apropriados do que os recursos para uma linguagem completamente diferente, por exemplo, inglês (Estados Unidos), que são os únicos outros fallbacks possíveis.

Como outro exemplo, um aplicativo pode não ser localizado para o Belize. No entanto, o suporte à preferência de idioma Inglês (Belize), representado como en-por, permite que o aplicativo volte para os recursos "en".

## <a name="language-fallback-in-the-resource-loader"></a>Fallback de idioma no carregador de recursos

O Windows Vista e posterior organizam as configurações de idioma da interface do usuário em uma lista de idiomas de fallback em ordem deordenada usada pelo carregador de recursos. Para formar a lista, o sistema operacional combina vários idiomas, na ordem mostrada:

-   Linguagens de interface do usuário preferencial de thread, que consistem em linguagem de interface e sua forma neutra. Os exemplos são fr-FR para francês (França) e sua forma neutra "fr" e es-ES para espanhol (Espanha) e sua forma neutra "es".
-   Processe linguagens de interface do usuário preferenciais, que consistem em processar o idioma da interface e sua forma neutra. Um exemplo é de-de para alemão (Alemanha) e sua forma neutra "de".
-   Idioma da interface do usuário e sua forma neutra. Um exemplo é ja-JP para japonês (Japão) e sua forma neutra "ja".
-   Idioma da interface do usuário do sistema e sua forma neutra. Um exemplo é it-it para italiano (Itália) e sua forma neutra "It".
    > [!Note]  
    > Esse idioma só é incluído na lista de fallback quando o idioma da interface do usuário não está definido.

     

-   Idioma da interface do usuário padrão do sistema e sua forma neutra. Um exemplo é es-ES para espanhol (Espanha) e sua forma neutra "es".

O seguinte mostra a lista de fallback mesclada. Observe que a duplicação de idiomas, por exemplo, es-ES e es, é eliminada. Como o exemplo define o idioma da interface do usuário para ja-JP, o idioma da interface de usuário do sistema não aparece na lista de fallback mesclada.

fr-FR, FR, es-ES, es, de-DE, de, ja-JP, ja

Ao carregar recursos para um aplicativo MUI, o carregador de recursos tenta selecionar um dos arquivos que correspondem à lista de idiomas da interface do usuário preferencial do thread para o thread do aplicativo em execução no momento. Se o carregador de recursos não conseguir localizar uma correspondência direta entre um idioma selecionado e o primeiro recurso específico de idioma na lista de fallback mesclada, ele verificará os idiomas subsequentes na lista até encontrar um fallback aceitável.

Se o carregador de recursos não encontrar nenhum arquivo necessário, ele deverá usar uma linguagem de fallback "boa garantia". Para a tecnologia de recursos do MUI, o carregador de recursos determina o idioma de fallback dos dados de configuração de recursos fornecidos. Para obter mais informações, consulte [Gerenciamento de recursos do MUI](mui-resource-management.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a interface do usuário multilíngue](about-multilingual-user-interface.md)
</dt> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Terminologia do NLS](nls-terminology.md)
</dt> </dl>

 

 



