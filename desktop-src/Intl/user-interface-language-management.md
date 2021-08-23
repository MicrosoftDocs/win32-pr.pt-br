---
description: A MUI permite que seus aplicativos gerenciem linguagens de interface do usuário de duas maneiras.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Interface do Usuário de linguagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaf20ca6183109f81572eeb706673812fc988eca87ea2522f437eafd22774b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631836"
---
# <a name="user-interface-language-management"></a>Interface do Usuário de linguagem

A MUI permite que seus aplicativos gerenciem linguagens de interface do usuário de duas maneiras. Um aplicativo pode usar uma abordagem simples para o gerenciamento de idioma por padrão para as configurações de idioma do sistema operacional. Como alternativa, o aplicativo pode dar suporte a seus próprios idiomas dos quais o usuário pode selecionar. A API de MUI também permite que seu aplicativo acesse diretamente idiomas e listas de idiomas com suporte pelo sistema operacional e mantido pelo carregador de recursos. O restante deste tópico define os idiomas com suporte do sistema e o mecanismo de fallback de idioma.

## <a name="languages-maintained-by-the-operating-system"></a>Idiomas mantidos pelo sistema operacional

### <a name="system-default-ui-languageinstall-language"></a>Idioma da interface do usuário padrão do sistema/idioma de instalação

O idioma de interface do usuário padrão do sistema é o idioma da versão localizada usada para configurar Windows. Todos os menus, caixas de diálogo, mensagens de erro e arquivos de ajuda são representados nesse idioma, exceto quando o usuário seleciona um idioma diferente.

No Windows Vista e posterior, a linguagem de interface do usuário padrão do sistema é conhecida como a "linguagem de instalação" e desempenha uma função mais limitada. Para a maioria das finalidades, ela é superada pelos idiomas de interface do usuário preferenciais do sistema. No entanto, em determinados contextos, é útil ter uma única linguagem de instalação que sempre tenha suporte total.

Nenhuma função de MUI está disponível para definir a linguagem de interface do usuário padrão do sistema. Para recuperar esse idioma, o aplicativo pode chamar [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Linguagem de interface do usuário do sistema

O sistema operacional define a linguagem de interface do usuário do sistema  como uma linguagem de interface do usuário que pode ser definida por um administrador na guia Avançado da parte de opções regionais e de idioma do Painel de Controle. O sistema operacional usará esse idioma se o usuário atual não tiver feito configurações específicas de idioma ou se nenhuma conta ativa estiver conectado. O idioma poderá ser alterado somente se mais de uma linguagem de interface do usuário estiver instalada no computador.

> [!Note]  
> O sistema operacional deve ser reinicializado para que todos os usuários e serviços vejam o efeito da alteração de idioma.

 

Nenhuma função de MUI está disponível para definir a linguagem de interface do usuário do sistema. Para recuperar esse valor, um aplicativo direcionado ao Windows Vista e posterior pode chamar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e obter o primeiro idioma na lista de idiomas de interface do usuário preferenciais do sistema. Aplicativos direcionados a sistemas operacionais do Vista pré-Windows não podem usar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) e devem se basear na suposição de que a linguagem de interface do usuário do sistema é sempre a mesma que a linguagem de interface do usuário padrão do sistema.

### <a name="user-ui-language"></a>Idioma da interface do usuário do usuário

A linguagem de interface do usuário determina a linguagem de interface do usuário usada para menus, caixas de diálogo, arquivos de ajuda e assim por diante. Ele pode ser definido pelo  usuário atual na guia Idioma da parte de opções regionais e de idioma do Painel de Controle. Esse idioma só poderá ser alterado se mais de uma linguagem de interface do usuário estiver instalada no computador. Observe que o usuário terá que fazer logoff e, em seguida, fazer logoff novamente para ver o efeito. Por exemplo, uma empresa multinacional deseja implantar Windows em todas as suas subsidiárias. A empresa cria um trabalho de instalação global, que instala a versão de idioma inglês do Windows em todos os clientes, independentemente do local. Ao mesmo tempo, ele instala módulos de idioma específicos, dependendo da unidade organizacional da qual um computador é membro. Quando o usuário faz logor na primeira vez em um sistema operacional recém-instalado, Windows aparece como uma versão localizada.

No Windows Vista e posterior, o idioma da interface do usuário é o primeiro idioma na lista de idiomas de interface do usuário preferenciais. Observe que os idiomas de fallback podem ser usados se recursos específicos não estão disponíveis neste idioma.

Em sistemas operacionais Windows Vista, a linguagem de interface do usuário do usuário geralmente é a mesma que a linguagem de interface do usuário padrão do sistema. No entanto, Windows MUI, os dois idiomas podem ser diferentes.

Para recuperar a linguagem de interface do usuário, um aplicativo pode chamar [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) ou [**GetUserPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages) O aplicativo não pode alterar o idioma da interface do usuário, pois não há nenhuma função para defini-lo.

## <a name="language-lists-maintained-by-the-operating-system"></a>Listas de idiomas mantidas pelo sistema operacional

### <a name="system-preferred-ui-languages-list"></a>Lista de idiomas de interface do usuário preferenciais do sistema

O carregador de recursos mantém uma lista de idiomas de interface do usuário preferenciais do sistema. Incluídos nesta lista são idiomas preferenciais do sistema operacional para seus próprios recursos, como menus e caixas de diálogo, mensagens, arquivos INF e arquivos de ajuda. A lista é feita pela linguagem de interface do usuário padrão do sistema e pelo idioma da interface do usuário do sistema e seus fallbacks. Um aplicativo pode recuperar idiomas de interface do usuário preferenciais do sistema chamando [**GetSystemPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)

### <a name="user-preferred-ui-languages-list"></a>Lista de idiomas de interface do usuário preferenciais do usuário

O carregador de recursos usa uma lista de idiomas de interface do usuário preferenciais que inclui idiomas que o usuário prefere. O carregador de recursos usa recursos correspondentes a idiomas dessa lista, se disponível, para um thread de aplicativo específico. Esses idiomas têm precedência sobre as preferências do sistema. Para recuperar idiomas de interface do usuário preferenciais, seu aplicativo pode [**chamar GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Lista de idiomas de interface do usuário preferenciais do processo

No Windows Vista e posterior, o carregador de recursos mantém uma lista de idiomas de interface do usuário preferenciais do processo que consiste em até cinco idiomas válidos definidos por um processo em execução para um aplicativo de MUI. Os idiomas podem ser definidos pelo aplicativo com uma chamada para [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). O aplicativo pode recuperar os idiomas chamando [**GetProcessPreferredUILanguages.**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages)

### <a name="thread-preferred-ui-languages-list"></a>Lista de idiomas de interface do usuário preferenciais do thread

No Windows Vista e posterior, o carregador de recursos usa uma lista de idiomas de interface do usuário preferenciais de thread que consiste em até cinco idiomas válidos definidos por um thread em um processo em execução para um aplicativo de MUI. Essas linguagens são usadas para personalizar as linguagens de interface do usuário do aplicativo e torná-las diferentes da linguagem do sistema operacional. A lista de idiomas de interface do usuário preferencial do thread baseia-se nos idiomas de interface do usuário preferenciais do usuário, nos idiomas de interface do usuário preferenciais do sistema e no idioma de interface do usuário padrão do sistema.

Para definir os idiomas de interface do usuário preferenciais do thread, o aplicativo deve chamar [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Para recuperar esses idiomas, o aplicativo [**chama GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Representação de idioma neutro

Um idioma neutro é representado como o idioma sozinho, sem região ou localidade. Por exemplo, a representação neutra do idioma inglês (Canadá), en-CA, é representada como "en". Embora um idioma neutro não seja associado aos aspectos de uma região ou localidade, você pode associá-lo a um conjunto de recursos. Normalmente, um recurso de idioma neutro baseia-se no uso na região mais predominante para o idioma.

Como ilustração, suponha que seu aplicativo MUI localize recursos de idioma alemão para alemão (Suíça) representados como de-CH e alemão (Suíça) representados como de-AT, ao criar um conjunto completo de recursos para alemão (Alemanha) representados como de-DE. Você deve tomar decisões para esse aplicativo considerando arquivos de recursos inteiros. Se o aplicativo duplicar os recursos de de-DE como recursos de idioma neutros, ele deverá fornecer um idioma de fallback para o carregador de recursos. Se o carregador não encontrar um arquivo de recurso específico de idioma específico para de-CH ou para de-AT, ele voltará para os recursos "de" neutros em idioma. Esses recursos provavelmente são mais apropriados do que os recursos para um idioma completamente diferente, por exemplo, inglês (Estados Unidos), que são os únicos outros fallbacks possíveis.

Como outro exemplo, um aplicativo pode não ser localizado para o Quel. No entanto, o suporte a uma preferência de idioma de inglês (English), representada como en-BZ, permite que o aplicativo volte para recursos "en".

## <a name="language-fallback-in-the-resource-loader"></a>Fallback de idioma no Carregador de Recursos

Windows O Vista e posterior organizam as configurações de idioma da interface do usuário em uma lista de idiomas de fallback pré-organizada usada pelo carregador de recursos. Para formar a lista, o sistema operacional combina vários idiomas, na ordem mostrada:

-   Idiomas de interface do usuário preferenciais do thread, que consistem em linguagem de interface do usuário do thread e sua forma neutra. Exemplos são fr-FR para francês (França) e sua forma neutra "fr" e es-ES para espanhol (Espanha) e sua forma neutra "es".
-   Processe linguagens de interface do usuário preferenciais, consistindo em linguagem de interface do usuário de processo e sua forma neutra. Um exemplo é de-DE para alemão (Alemanha) e sua forma neutra "de".
-   Idioma da interface do usuário do usuário e sua forma neutra. Um exemplo é ja-JP para japonês (Japão) e sua forma neutra "ja".
-   Idioma da interface do usuário do sistema e sua forma neutra. Um exemplo é it-IT para italiano (Itália) e sua forma neutra "it".
    > [!Note]  
    > Esse idioma só é incluído na lista de fallback quando o idioma da interface do usuário não está definido.

     

-   Idioma de interface do usuário padrão do sistema e sua forma neutra. Um exemplo é es-ES para espanhol (Espanha) e sua forma neutra "es".

O exemplo a seguir mostra a lista de fallback mesclada. Observe que a duplicação de idiomas, por exemplo, es-ES e es, é eliminada. Como o exemplo define o idioma da interface do usuário como ja-JP, o idioma da interface do usuário do sistema não aparece na lista de fallback mesclada.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Ao carregar recursos para um aplicativo MUI, o carregador de recursos tenta selecionar um dos arquivos correspondentes à lista de idiomas de interface do usuário preferenciais do thread para o thread de aplicativo em execução no momento. Se o carregador de recursos não puder encontrar uma combinação direta entre um idioma selecionado e o primeiro recurso específico do idioma na lista de fallback mesclada, ele verificará os idiomas subsequentes na lista até encontrar um fallback aceitável.

Se o carregador de recursos não encontrar nenhum arquivo necessário, ele deverá usar uma linguagem de fallback "garantida boa". Para a tecnologia de recursos da MUI, o carregador de recursos determina o idioma de fallback dos dados de configuração de recurso fornecidos. Para obter mais informações, consulte [MUI Resource Management](mui-resource-management.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Interface de Usuário Multilíngue](about-multilingual-user-interface.md)
</dt> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Terminologia de NLS](nls-terminology.md)
</dt> </dl>

 

 



