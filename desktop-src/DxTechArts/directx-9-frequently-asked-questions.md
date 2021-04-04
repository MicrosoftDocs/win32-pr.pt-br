---
title: Perguntas frequentes sobre o DirectX
description: Este artigo contém uma coleção de perguntas frequentes sobre o Microsoft DirectX.
ms.assetid: 58d9fe45-a2c7-8280-2826-e2e14ecea983
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd5fd70f1a651121b8d977dbb9479cef6edd024
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007829"
---
# <a name="directx-frequently-asked-questions"></a>Perguntas frequentes sobre o DirectX

Este artigo contém uma coleção de perguntas frequentes sobre o Microsoft DirectX.

-   [Problemas gerais de desenvolvimento do DirectX](#general-directx-development-issues)
-   [Perguntas sobre o Direct3D](#direct3d-questions)
    -   [Perguntas gerais sobre o Direct3D](#general-direct3d-questions)
    -   [Processamento de geometria (vértice)](#geometry-vertex-processing)
    -   [Ajuste de desempenho](#performance-tuning)
    -   [Biblioteca do utilitário D3DX](#d3dx-utility-library)
-   [Perguntas sobre o DirectSound](#directsound-questions)
-   [Extensões do DirectX para Alias Maya](#directx-extensions-for-alias-maya)
-   [Perguntas XInputs](#xinput-questions)

## <a name="general-directx-development-issues"></a>Problemas gerais de desenvolvimento do DirectX

<dl> <dt>

<span id="Should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="SHOULD_GAME_DEVELOPERS_REALLY_CARE_ABOUT_SUPPORTING_X64_EDITIONS_"></span>**Os desenvolvedores de jogos devem realmente se preocupar com o suporte a edições x64?**
</dt> <dd>

Com certeza. a tecnologia x64 está amplamente disponível no mercado. A maioria das novas CPUs vendidas nos últimos anos, e quase todas as linhas de processador em desenvolvimento da AMD e da Intel, são compatíveis com x64. O Windows XP Professional x64 Edition introduziu a tecnologia de habilitação do sistema operacional para x64 lançada em abril de 2005. Como as edições x64 exigem uma nova geração de drivers nativos de 64 bits, essa primeira versão era limitada à distribuição OEM.

Com o Windows Vista, os clientes são livres para escolher as edições de 32 bits ou 64 bits ao comprar computadores baseados no Windows, e as licenças para o Windows Vista são válidas para as edições de 32 bits ou de 64 bits do sistema operacional. Além disso, muitos drivers de 64 bits estão disponíveis na caixa, e os fabricantes de dispositivos são necessários para fornecer drivers nativos de 32 bits e de 64 bits como parte do programa de certificação do Windows.

Todos esses fatores aumentarão muito as implantações das edições de 64 bits do Windows. À medida que novos computadores começam a ser entregues com mais de 2 GB de RAM física, o incentivo para usar um sistema operacional de 32 bits diminui bastante em favor das edições de 64 bits. A tecnologia de 64 bits dá suporte total a código nativo de 32 bits, embora as implementações nativas de 64 bits sejam necessárias para aproveitar ao máximo o novo espaço de memória de 64 bits. Cada aplicativo de 32 bits deve ter compatibilidade de 64 bits como um requisito mínimo de envio e atender a esse requisito é um requisito de linha de base para a compatibilidade com o Windows Vista. As incompatibilidades normalmente surgem do uso de código de 16 bits projetados para o sistema operacional Windows 3,1 ou a instalação de drivers que não são fornecidos em formulários nativos de 32 bits e 64 bits.

Para obter mais detalhes sobre a tecnologia de 64 bits, consulte [programação de 64 bits para desenvolvedores de jogos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_95__Windows_98_or_Windows_ME_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_95__windows_98_or_windows_me_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_95__WINDOWS_98_OR_WINDOWS_ME_"></span>**Os desenvolvedores de jogos ainda estão publicando jogos para Windows 95, Windows 98 ou Windows ME?**
</dt> <dd>

Não é mais por dois motivos: desempenho e conjunto de recursos.

Se a velocidade mínima da CPU necessária para seu jogo for de 1,2 GHz ou superior (o que é mais comum para títulos de alto desempenho), a grande maioria dos computadores qualificados estará executando o Windows XP. No momento em que os computadores com velocidades de CPU acima de 1,2 GHz foram vendidos, o Windows XP foi instalado como o sistema operacional padrão por quase todos os fabricantes. Isso significa que há muitos recursos encontrados no Windows XP que os desenvolvedores de jogos atuais devem aproveitar, incluindo:

-   Multitarefas aprimoradas – o que resulta em uma experiência melhor e mais suave para vídeo, áudio e jogos.
-   Modelo de driver de vídeo mais estável, que permite depuração mais fácil, reprodução de jogos mais suave e melhor desempenho.
-   Configuração mais fácil para rede – que permite o acesso mais fácil a jogos de vários jogadores.
-   Suporte para transferências DMA por padrão de discos rígidos, o que resulta em aplicativos de carregamento mais suaves e mais rápidos.
-   Relatório de erros do Windows-que resulta em um sistema operacional, drivers e aplicativos mais estáveis.
-   Suporte a Unicode – que simplifica muito os problemas de localização.
-   Melhor segurança e estabilidade – o que resulta em melhores experiências do consumidor.
-   Melhor suporte para hardware moderno – a maior parte dos quais não usa mais drivers do Windows 98.
-   Melhor gerenciamento de memória-o que resulta em maior estabilidade e segurança.
-   Sistema de arquivos NTFS aprimorado-que é mais resistente a falhas e tem melhor desempenho com recursos de segurança.

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_2000_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_2000_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_2000_"></span>**Os desenvolvedores de jogos ainda estão publicando jogos para o Windows 2000?**
</dt> <dd>

Não mais. Além dos motivos listados em, **os desenvolvedores de jogos ainda estão publicando jogos para windows 95, windows 98 ou Windows me?**, o Windows 2000 não tem esses recursos:

-   O Windows XP dá suporte a recursos avançados de processador, como hiperthreading, vários núcleos e x64.
-   O Windows XP dá suporte a componentes lado a lado que reduz significativamente os conflitos de controle de versão do aplicativo.
-   O Windows XP dá suporte à proteção de memória sem execução que ajuda a impedir programas mal-intencionados e pode auxiliar a depuração.
-   O Windows XP melhorou o suporte para placas de vídeo avançadas baseadas em AGP e PCI Express.
-   O Windows XP dá suporte à troca rápida de usuários, à área de trabalho remota e à assistência remota, o que pode ajudar a reduzir os custos de suporte
-   Ferramentas de desempenho como o PIX (no SDK para desenvolvedores do DirectX) não oferecem mais suporte ao Windows 2000.

Em suma, o Windows 2000 nunca foi projetado ou comercializado como um sistema operacional de consumidor.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_Vista__How_do_they_impact_my_DirectX_application_"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_vista__how_do_they_impact_my_directx_application_"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_VISTA__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION_"></span>**Quais são as diferenças entre as várias edições do Windows Vista? Como eles afetam meu aplicativo DirectX?**
</dt> <dd>

A família Windows Vista inclui cinco edições:

-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Business
-   Windows Vista Enterprise
-   Windows Vista Ultimate

O Home Basic e o Home Premium são versões focadas no consumidor, com recursos como a segurança da família (anteriormente conhecido como controles dos pais), e o Home Premium inclui o Media Center. Business e Enterprise são edições com foco corporativo, com recursos como ingresso no domínio e serviços de Área de Trabalho Remota/terminal. A edição definitiva combina todos os recursos do consumidor e das edições corporativas em uma única versão. Todas as edições são fornecidas em edições de 32 bits (x86) e 64 bits (x64), e os usuários são livres para usar o mesmo identificador de produto para ambas as plataformas.

A tecnologia subjacente às várias edições é idêntica e todas têm a mesma versão do tempo de execução do DirectX e outros componentes. No entanto, as edições têm algumas pequenas diferenças em relação aos jogos:

-   O explorador de jogos existe em todas as edições, mas o atalho jogos no menu iniciar só está no início básico, Home Premium e Ultimate. O explorador de jogos ainda pode ser encontrado em todas as edições (clicando em Iniciar, apontando para todos os programas e clicando em jogos) e a interface IGameExplorer em todas as edições.
-   Os jogos incluídos no Windows não estão disponíveis por padrão no Business e Enterprise, mas podem ser habilitados pelo administrador.
-   A segurança da família e as classificações de jogos não exibem nem influenciam o comportamento do negócio ou da empresa, e elas são desabilitadas no Ultimate quando um domínio é Unido.

As configurações de controle de conta de usuário têm os mesmos padrões em todas as edições, mas podem ser substituídas pelas configurações de Política de Grupo para o domínio em Business, Enterprise e Ultimate. Por exemplo, a configuração de política controle de conta de usuário: o comportamento da solicitação de elevação para usuários padrão pode ser bem definido para negar automaticamente as solicitações de elevação em muitas configurações de negócios para aumentar a segurança, e muitos usuários nesses ambientes sempre serão executados como usuários padrão sem a possibilidade de optar por executar como administrador. Qualquer programa (como um instalador) que exija direitos administrativos, devido à detecção de configuração herdada ou a um manifesto que especifica o nível de execução solicitado como "requireAdministrator", sempre falhará ao iniciar nessas situações. Outras configurações de política, como o controle de conta de usuário: só eleva os executáveis assinados e validados, também podem impedir que o instalador funcione se você não assinar o arquivo executável usando Authenticode.

Esses tipos de alterações de diretiva podem ser aplicados a qualquer edição do Windows Vista, mas são mais prováveis em computadores que ingressaram em um domínio.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_7__How_do_they_impact_my_DirectX_application__"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_7__how_do_they_impact_my_directx_application__"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_7__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION__"></span>**Quais são as diferenças entre as várias edições do Windows 7? Como eles afetam meu aplicativo DirectX?** 
</dt> <dd>

A maioria dos usuários do Windows 7 provavelmente terá uma das duas edições: Windows 7 Home Premium, para usuários domésticos ou Windows 7 Professional, para usuários e desenvolvedores comerciais. Para grandes corporações, há o Windows 7 Enterprise Edition licenciado por volume, que inclui todos os recursos do Windows 7; O Windows 7 Ultimate é o equivalente de varejo dessa edição.

O Windows 7 Starter Edition está disponível em todo o mundo para os OEMs, e é esperado que ele seja implantado primarly com os computadores notebook de ultra baixa energia. O Windows 7 Home Basic está disponível apenas em mercados emergentes.

Observe que todas as edições do Windows 7 (exceto Starter Edition) estão disponíveis para versões de 32 bits (x86) e 64 (x64), e todos os pacotes de varejo do Windows 7 incluem mídia para ambas as versões. Assim como no Windows Vista, os usuários são livres para usar o mesmo identificador de produto de varejo em qualquer plataforma.

A tecnologia subjacente nas várias edições é idêntica e todas as edições têm a mesma versão do tempo de execução do DirectX e outros componentes. Eles têm algumas diferenças em relação aos recursos de jogos:

-   O explorador de jogos existe em todas as edições, mas o atalho jogos no menu iniciar está oculto por padrão no Windows 7 Professional e Enterprise. O explorador de jogos ainda pode ser encontrado no menu iniciar (clicando em todos os programas e clicando duas vezes em jogos) e o atalho de jogos diretos pode ser habilitado pelo usuário.
-   Os jogos incluídos no Windows não estão disponíveis por padrão no Windows 7 Professional e Enterprise, mas podem ser habilitados pelo administrador.
-   As classificações de jogos e de segurança da família estão disponíveis em todas as edições, mas estão desabilitadas no Windows 7 Professional, Enterprise e Ultimate quando o sistema operacional ingressa em um domínio. Assim como no Windows Vista Ultimate, esse recurso pode ser habilitado novamente no computador que ingressou em um domínio.

As configurações do controle de conta de usuário (UAC) podem ser afetadas pelas configurações de Política de Grupo nas edições Professional, Enterprise e Ultimate do Windows 7, muito parecidas com o Windows Vista. Para obter mais informações, consulte **quais são as diferenças entre as várias edições do Windows Vista? Como eles afetam meu aplicativo DirectX?**

</dd> <dt>

<span id="Will_DirectX_10_be_available_for_Windows_XP__"></span><span id="will_directx_10_be_available_for_windows_xp__"></span><span id="WILL_DIRECTX_10_BE_AVAILABLE_FOR_WINDOWS_XP__"></span>**O DirectX 10 estará disponível para o Windows XP?** 
</dt> <dd>

Não. O Windows Vista, que tem o DirectX 10, inclui um tempo de execução do DirectX atualizado com base no tempo de execução do Windows XP SP2 (DirectX 9.0 c) com alterações para trabalhar com o novo Windows Display Driver Model (WDDM) e a nova pilha de drivers de áudio, e com outras atualizações no sistema operacional. Além do Direct3D 9, o Windows Vista dá suporte a duas novas interfaces quando o hardware e os drivers de vídeo corretos estão presentes: Direct3D9Ex e Direct3D10.

Como essas novas interfaces dependem da tecnologia WDDM, elas nunca estarão disponíveis em versões anteriores do Windows. Todas as outras alterações feitas nas tecnologias DirectX para o Windows Vista também são específicas para a nova versão do Windows. O nome DirectX 10 é enganoso, pois muitas tecnologias que são fornecidas no SDK do DirectX (transação, XINPUT, D3DX) não são incluídas por esse número de versão. Portanto, fazer referência ao número de versão do tempo de execução do DirectX como um todo perdeu muito de seu significado, mesmo para o 9.0 c. A ferramenta de diagnóstico do DirectX (DXdiag.exe) no Windows Vista relata o DirectX 10, mas isso realmente se refere apenas ao Direct3D 10.

</dd> <dt>

<span id="Will_DirectX_11_be_available_for_Windows_Vista_or_Windows_XP__"></span><span id="will_directx_11_be_available_for_windows_vista_or_windows_xp__"></span><span id="WILL_DIRECTX_11_BE_AVAILABLE_FOR_WINDOWS_VISTA_OR_WINDOWS_XP__"></span>**O DirectX 11 estará disponível para o Windows Vista ou o Windows XP?** 
</dt> <dd>

O DirectX 11 é integrado ao Windows 7 e está disponível como uma atualização para o Windows Vista (consulte <https://go.microsoft.com/fwlink/p/?linkid=160189> ). Isso inclui a API do Direct3D 11, o DXGI (infraestrutura de gráficos do DirectX) 1,1, os níveis de recursos do 10Level9, o dispositivo de renderização da plataforma de rasterização avançada do Windows (WARP) 10, o Direct2D, o DirectWrite e uma atualização para a API do Direct3D 10,1 para dar suporte a 10Level9 e WARP 10.

Pelos mesmos motivos indicados na pergunta anterior (o **DirectX 10 estará disponível para o Windows XP?** ), O Direct3D 11 e as APIs relacionadas não estão disponíveis no Windows XP.

</dd> <dt>

<span id="What_Happened_to_DirectShow__I_can_t_find_it_in_the_DirectX_SDK._"></span><span id="what_happened_to_directshow__i_can_t_find_it_in_the_directx_sdk._"></span><span id="WHAT_HAPPENED_TO_DIRECTSHOW__I_CAN_T_FIND_IT_IN_THE_DIRECTX_SDK._"></span>**O que aconteceu com o DirectShow? Não consigo encontrá-lo no SDK do DirectX.** 
</dt> <dd>

O DirectShow foi removido do SDK do DirectX a partir de abril de 2005. Você pode obter os cabeçalhos, bibliotecas, ferramentas e exemplos do DirectShow no kit de desenvolvimento de software do Windows (anteriormente conhecido como SDK da plataforma). O DirectSetup no SDK do DirectX continua a dar suporte à redistribuição dos componentes do sistema do DirectShow, e os componentes mais recentes já estão instalados nos seguintes sistemas operacionais: Microsoft Windows XP Service Pack 2, Windows XP Professional x64 Edition, Windows Server 2003 Service Pack 1 e Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_Vista__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_vista__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_VISTA__"></span>**Quais alterações foram feitas no tempo de execução do DirectX para o Windows Vista?** 
</dt> <dd>

As principais alterações foram feitas para dar suporte ao novo WDDM. Para obter detalhes sobre o novo modelo de driver, sobre os impactos no Direct3D 9 e nas duas novas interfaces gráficas, Direct3D 9Ex e Direct3D 10, examine as [APIs de gráficos no Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista). Novas APIs de gráficos para o Windows 7 – Direct3D 11, Direct2D, DirectWrite, DXGI 1,1 e um Direct3D 10.1 atualizado — estão disponíveis como uma atualização para o Windows Vista (consulte <https://go.microsoft.com/fwlink/p/?linkid=160189> ).

O Windows Vista Service Pack 1 inclui uma versão atualizada do tempo de execução do DirectX. Essa atualização estende o suporte do Windows Vista para incluir o Direct3D 10,1, expondo novos recursos de hardware opcionais. (Todo o hardware que é capaz de dar suporte ao Direct3D 10,1 também dá suporte completo a todos os recursos do Direct3D 10.)

O DirectSound foi atualizado para expor os recursos da nova pilha de drivers de áudio do Windows Vista, que dá suporte a buffers de software de vários canais. A API do modo retido do Direct3D foi completamente removida do Windows Vista. O DirectPlay Voice também foi removido, bem como o auxiliar NAT do DirectPlay e a interface do usuário do mapeador de ação do DirectInput. O suporte para as interfaces DirectX 7 e DirectX 8 para Visual Basic 6,0 não está disponível no Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_7__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_7__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_7__"></span>**Quais alterações foram feitas no tempo de execução do DirectX para o Windows 7?** 
</dt> <dd>

O Windows 7 inclui todos os componentes de tempo de execução do DirectX encontrados no Windows Vista e adiciona os níveis de recurso do Direct3D 11, DXGI 1,1, 10Level9, o dispositivo WARP10 software, o Direct2D, o DirectWrite e uma atualização para o Direct3D 10,1 para dar suporte a 10Level9 e WARP10. Para obter mais informações, consulte [APIs de gráficos no Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista).

Todos os outros componentes são idênticos ao Windows Vista, com a adição de suporte nativo de 64 bits (x64) para a API principal do DirectMusic relacionada à MIDI com carimbo de data/hora. A camada de desempenho do DirectMusic permanece preterida e está disponível somente para aplicativos de 32 bits no Windows 7 para compatibilidade de aplicativos. Observe que o suporte nativo de 64 bits do DirectMusic não está disponível no Windows Vista.

</dd> <dt>

<span id="I_think_I_have_found_a_driver_bug__what_do_I_do__"></span><span id="i_think_i_have_found_a_driver_bug__what_do_i_do__"></span><span id="I_THINK_I_HAVE_FOUND_A_DRIVER_BUG__WHAT_DO_I_DO__"></span>**Acho que encontrei um bug de driver, o que eu faço?** 
</dt> <dd>

Primeiro, verifique se você verificou os resultados com o rasterizador de referência. Em seguida, verifique os resultados com a versão mais recente certificada pelo WHQL do driver do IHVs. Você pode verificar programaticamente o status do WHQL usando o método GetAdapterIdentifier () na interface IDirect3D9 passando \_ o \_ sinalizador nível de WHQL D3DENUM.

</dd> <dt>

<span id="Why_do_I_get_so_many_error_messages_when_I_try_to_compile_the_samples__"></span><span id="why_do_i_get_so_many_error_messages_when_i_try_to_compile_the_samples__"></span><span id="WHY_DO_I_GET_SO_MANY_ERROR_MESSAGES_WHEN_I_TRY_TO_COMPILE_THE_SAMPLES__"></span>**Por que obtenho tantas mensagens de erro quando tento compilar os exemplos?** 
</dt> <dd>

Você provavelmente não tem o caminho de inclusão definido corretamente. Muitos compiladores, incluindo Microsoft Visual C++, incluem uma versão anterior do SDK, portanto, se o caminho de inclusão Pesquisar o compilador padrão, inclua os diretórios primeiro, você obterá versões incorretas dos arquivos de cabeçalho. Para corrigir esse problema, verifique se o caminho de inclusão e os caminhos de biblioteca estão definidos para pesquisar o Microsoft DirectX include e os caminhos de biblioteca primeiro. Consulte também o arquivo dxreadme.txt no SDK. Se você instalar o SDK do DirectX e estiver usando Visual C++, o instalador poderá, opcionalmente, configurar os caminhos de inclusão para você.

</dd> <dt>

<span id="I_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__GUIDs___what_do_I_do__"></span><span id="i_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__guids___what_do_i_do__"></span><span id="I_GET_LINKER_ERRORS_ABOUT_MULTIPLE_OR_MISSING_SYMBOLS_FOR_GLOBALLY_UNIQUE_IDENTIFIERS__GUIDS___WHAT_DO_I_DO__"></span>**Obtenho erros de vinculador sobre os símbolos múltiplos ou ausentes para identificadores (GUIDs) globalmente exclusivos, o que eu faço?** 
</dt> <dd>

Os vários GUIDs que você usa devem ser definidos uma vez e apenas uma vez. A definição do GUID será inserida se você \# definir o símbolo Initguid antes de incluir os arquivos de cabeçalho do DirectX. Portanto, você deve certificar-se de que isso ocorre apenas para uma unidade de compilação. Uma alternativa para esse método é vincular com a biblioteca dxguid. lib, que contém definições para todos os GUIDs do DirectX. Se você usar esse método (recomendado), você nunca deve \# definir o símbolo Initguid.

</dd> <dt>

<span id="Can_I_cast_a_pointer_to_a_DirectX_interface_to_a_lower_version_number__"></span><span id="can_i_cast_a_pointer_to_a_directx_interface_to_a_lower_version_number__"></span><span id="CAN_I_CAST_A_POINTER_TO_A_DIRECTX_INTERFACE_TO_A_LOWER_VERSION_NUMBER__"></span>**Posso converter um ponteiro para uma interface DirectX em um número de versão inferior?** 
</dt> <dd>

Não. As interfaces do DirectX são interfaces COM. Isso significa que não há nenhum requisito para que interfaces numeradas mais altas sejam derivadas de números menores correspondentes. Portanto, a única maneira segura de obter uma interface diferente para um objeto DirectX é usar o método QueryInterface da interface. Esse método faz parte da interface IUnknown padrão, da qual todas as interfaces COM devem derivar.

</dd> <dt>

<span id="Can_I_mix_the_use_of_DirectX_9_components_and_DirectX_8_or_earlier_components_within_the_same_application__"></span><span id="can_i_mix_the_use_of_directx_9_components_and_directx_8_or_earlier_components_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECTX_9_COMPONENTS_AND_DIRECTX_8_OR_EARLIER_COMPONENTS_WITHIN_THE_SAME_APPLICATION__"></span>**Posso misturar o uso de componentes DirectX 9 e DirectX 8 ou componentes anteriores no mesmo aplicativo?** 
</dt> <dd>

Você pode misturar livremente diferentes componentes da versão diferente; por exemplo, você poderia usar o DirectInput 8 com o Direct3D 9 no mesmo aplicativo. No entanto, geralmente não é possível misturar versões diferentes do mesmo componente dentro do mesmo aplicativo; por exemplo, você não pode misturar o DirectDraw 7 com o Direct3D 9 (já que eles são efetivamente o mesmo componente que o DirectDraw foi incorporadas no Direct3D a partir do DirectX 8). No entanto, há exceções, como o uso do Direct3D 9 e do Direct3D 10 juntos no mesmo aplicativo, que é permitido.

</dd> <dt>

<span id="Can_I_mix_the_use_of_Direct3D_9_and_Direct3D_10_within_the_same_application__"></span><span id="can_i_mix_the_use_of_direct3d_9_and_direct3d_10_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECT3D_9_AND_DIRECT3D_10_WITHIN_THE_SAME_APPLICATION__"></span>**Posso misturar o uso do Direct3D 9 e do Direct3D 10 no mesmo aplicativo?** 
</dt> <dd>

Sim, você pode usar essas versões do Direct3D juntas no mesmo aplicativo.

</dd> <dt>

<span id="What_do_the_return_values_from_the_Release_or_AddRef_methods_mean__"></span><span id="what_do_the_return_values_from_the_release_or_addref_methods_mean__"></span><span id="WHAT_DO_THE_RETURN_VALUES_FROM_THE_RELEASE_OR_ADDREF_METHODS_MEAN__"></span>**O que significam os valores retornados dos métodos Release ou AddRef?** 
</dt> <dd>

O valor de retorno será a contagem de referência atual do objeto. No entanto, a especificação COM declara que você não deve contar com isso e o valor geralmente está disponível apenas para fins de depuração. Os valores que você observa podem ser inesperados, pois vários outros objetos do sistema podem estar mantendo referências aos objetos do DirectX que você criar. Por esse motivo, você não deve escrever código que chame repetidamente a liberação até que a contagem de referência seja zero, pois o objeto pode ser liberado mesmo que outro componente ainda possa fazer referência a ele.

</dd> <dt>

<span id="Does_it_matter_in_which_order_I_release_DirectX_interfaces__"></span><span id="does_it_matter_in_which_order_i_release_directx_interfaces__"></span><span id="DOES_IT_MATTER_IN_WHICH_ORDER_I_RELEASE_DIRECTX_INTERFACES__"></span>**Isso é importante na ordem em que as interfaces do DirectX são liberadas?** 
</dt> <dd>

Não se deve importar porque as interfaces COM são contadas como referência. No entanto, há alguns bugs conhecidos com a ordem de liberação das interfaces em algumas versões do DirectX. Para segurança, você é aconselhado a liberar interfaces na ordem de criação inversa quando possível.

</dd> <dt>

<span id="What_is_a_smart_pointer_and_should_I_use_it__"></span><span id="what_is_a_smart_pointer_and_should_i_use_it__"></span><span id="WHAT_IS_A_SMART_POINTER_AND_SHOULD_I_USE_IT__"></span>**O que é um ponteiro inteligente e devo usá-lo?** 
</dt> <dd>

Um ponteiro inteligente é uma classe de modelo C++ projetada para encapsular a funcionalidade do ponteiro. Em particular, há classes de ponteiro inteligente padrão projetadas para encapsular ponteiros de interface COM. Esses ponteiros executam automaticamente QueryInterface em vez de uma conversão e tratam AddRef e Release para você. Se você deve usá-los é basicamente uma questão de gosto. Se o seu código contiver muitas cópias de ponteiros de interface, com vários AddRefs e versões, os ponteiros inteligentes podem, provavelmente, tornar seu código mais organizado e menos propenso a erros. Caso contrário, você pode fazer isso sem eles. O Visual C++ inclui um apontador inteligente padrão da Microsoft, definido no arquivo de cabeçalho "comdef. h" (pesquise com \_ PTR \_ t na ajuda).

</dd> <dt>

<span id="I_have_trouble_debugging_my_DirectX_application__any_tips__"></span><span id="i_have_trouble_debugging_my_directx_application__any_tips__"></span><span id="I_HAVE_TROUBLE_DEBUGGING_MY_DIRECTX_APPLICATION__ANY_TIPS__"></span>**Tenho problemas para depurar meu aplicativo DirectX, dicas?** 
</dt> <dd>

O problema mais comum na depuração de aplicativos do DirectX é a tentativa de depurar enquanto uma superfície do DirectDraw está bloqueada. Essa situação pode causar um "bloqueio de Win16" nos sistemas Microsoft Windows 9x, o que impede que a janela do depurador seja pintada. Especificar o \_ sinalizador D3DLOCK NOSYSLOCK ao bloquear a superfície normalmente pode eliminar isso. O Windows 2000 não sofre desse problema. Ao desenvolver um aplicativo, é útil executá-lo com a versão de depuração do tempo de execução do DirectX (selecionado quando você instala o SDK), que executa alguma validação de parâmetro e gera mensagens úteis para a saída do depurador.

</dd> <dt>

<span id="What_s_the_correct_way_to_check_return_codes__"></span><span id="what_s_the_correct_way_to_check_return_codes__"></span><span id="WHAT_S_THE_CORRECT_WAY_TO_CHECK_RETURN_CODES__"></span>**Qual é a maneira correta de verificar códigos de retorno?** 
</dt> <dd>

Use as macros com êxito e com falha. Os métodos do DirectX podem retornar vários códigos de êxito e falha, portanto, é simples:

``` syntax
== D3D_OK
```

ou teste semelhante nem sempre será suficiente.

</dd> <dt>

<span id="How_do_I_disable_ALT_TAB_and_other_task_switching__"></span><span id="how_do_i_disable_alt_tab_and_other_task_switching__"></span><span id="HOW_DO_I_DISABLE_ALT_TAB_AND_OTHER_TASK_SWITCHING__"></span>**Como fazer desabilitar ALT + TAB e outros comutadores de tarefas?** 
</dt> <dd>

Você não tem! Os jogos precisam ser capazes de lidar com a alternância de tarefas normalmente, pois muitas coisas fazem com que isso aconteça: ALT + TAB, conexões de área de trabalho remota, troca rápida de usuário, limites de uso de controles dos pais e muitos outros eventos.

Ao mesmo tempo, duas fontes comuns de alternância acidental de tarefas em jogos com esquemas de controle centrado em teclado estão pressionando a tecla do logotipo do Windows e ativando as teclas de aderência do recurso de acessibilidade com a tecla SHIFT. Para resolver esses casos desabilitando a funcionalidade, consulte as técnicas descritas em [desabilitando as teclas de atalho em jogos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Is_there_a_recommended_book_explaining_COM__"></span><span id="is_there_a_recommended_book_explaining_com__"></span><span id="IS_THERE_A_RECOMMENDED_BOOK_EXPLAINING_COM__"></span>**Há um livro recomendado explicando COM?** 
</dt> <dd>

*Dentro de com* , Dale rogersment, publicada pela Microsoft Press, é uma excelente introdução ao com. Para obter uma visão mais detalhada do COM, o livro *Essential com* por Don Box, publicado por Longman, também é altamente recomendado.

</dd> <dt>

<span id="What_is_managed_code__"></span><span id="what_is_managed_code__"></span><span id="WHAT_IS_MANAGED_CODE__"></span>**O que é código gerenciado?** 
</dt> <dd>

Código gerenciado é o código que tem sua execução gerenciada pelo .NET Framework CLR (Common Language Runtime). Ele se refere a um contrato de cooperação entre o código de execução nativamente e o tempo de execução. Este contrato especifica que em qualquer ponto de execução, o tempo de execução pode parar uma CPU em execução e recuperar informações específicas para o endereço de instrução de CPU atual. As informações que devem ser habilitadas para consulta geralmente pertencem ao estado de tempo de execução, como registrar ou empilhar conteúdo de memória.

Antes da execução do código, o IL é compilado no código executável nativo. E, como essa compilação acontece pelo ambiente de execução gerenciado (ou, mais corretamente, por um compilador com reconhecimento de tempo de execução que sabe como direcionar o ambiente de execução gerenciado), o ambiente de execução gerenciado pode garantir o que o código vai fazer. Ele pode inserir interceptações e ganchos de coleta de lixo apropriados, manipulação de exceção, segurança de tipo, limites de matriz e verificação de índice e assim por diante. Por exemplo, tal compilador garante o layout de quadros de pilha e tudo o mais bem para que o coletor de lixo possa ser executado em segundo plano em um thread separado, movimentando constantemente a pilha de chamadas ativa, localizando todas as raízes, buscando todos os objetos ao vivo. Além disso, como o IL tem uma noção de segurança de tipo, o mecanismo de execução manterá a garantia de segurança de tipo, eliminando uma classe completa de erros de programação que geralmente levam a brechas de segurança.

Em contraste com isso com o mundo não gerenciado: arquivos executáveis não gerenciados são basicamente uma imagem binária, código x86, carregado na memória. O contador do programa é colocado lá e esse é o último que o sistema operacional sabe. Há proteções em vigor em relação ao gerenciamento de memória e à e/s de porta e assim por diante, mas o sistema não sabe realmente o que o aplicativo está fazendo. Portanto, ele não pode fazer nenhuma garantia sobre o que acontece quando o aplicativo é executado.

</dd> <dt>

<span id="What_books_are_there_about_general_Windows_programming__"></span><span id="what_books_are_there_about_general_windows_programming__"></span><span id="WHAT_BOOKS_ARE_THERE_ABOUT_GENERAL_WINDOWS_PROGRAMMING__"></span>**Quais livros estão lá sobre programação geral do Windows?** 
</dt> <dd>

Muitas. No entanto, os dois que são altamente recomendados são:

-   Programando janelas de Charles Petzold (Microsoft Press)
-   Programando aplicativos para Windows por Jeffrey Richter (Microsoft Press)

</dd> <dt>

<span id="How_do_I_debug_using_the_Windows_symbol_files__"></span><span id="how_do_i_debug_using_the_windows_symbol_files__"></span><span id="HOW_DO_I_DEBUG_USING_THE_WINDOWS_SYMBOL_FILES__"></span>**Como fazer depurar usando os arquivos de símbolo do Windows?** 
</dt> <dd>

A Microsoft publica símbolos removidos para todas as DLLs do sistema (mais algumas outras). Para acessá-los, adicione o seguinte ao seu caminho de símbolo nas configurações do projeto dentro do Visual Studio:

``` syntax
srv*https://msdl.microsoft.com/download/symbols
```

para armazenar em cache os símbolos localmente, use a seguinte sintaxe:

``` syntax
srv*c:\cache*https://msdl.microsoft.com/download/symbols
```

Em que c: \\ cache é um diretório local para arquivos de símbolo de cache.

</dd> </dl>

## <a name="direct3d-questions"></a>Perguntas sobre o Direct3D

### <a name="general-direct3d-questions"></a>Perguntas gerais sobre o Direct3D

<dl> <dt>

<span id="Where_can_I_find_information_about_3D_graphics_techniques__"></span><span id="where_can_i_find_information_about_3d_graphics_techniques__"></span><span id="WHERE_CAN_I_FIND_INFORMATION_ABOUT_3D_GRAPHICS_TECHNIQUES__"></span>**Onde posso encontrar informações sobre técnicas de gráficos 3D?** 
</dt> <dd>

O livro padrão sobre o assunto é gráfico de computador: princípios e prática de Foley, Van Dam et al. É um recurso valioso para qualquer pessoa que queira entender as bases matemáticas de geometria, rasterização e técnicas de iluminação. As perguntas frequentes para o grupo de Usenet comp. Graphics. Algorithms também contêm material útil.

</dd> <dt>

<span id="Does_Direct3D_emulate_functionality_not_provided_by_hardware__"></span><span id="does_direct3d_emulate_functionality_not_provided_by_hardware__"></span><span id="DOES_DIRECT3D_EMULATE_FUNCTIONALITY_NOT_PROVIDED_BY_HARDWARE__"></span>**O Direct3D emula a funcionalidade não fornecida pelo hardware?** 
</dt> <dd>

Depende. O Direct3D tem um pipeline de processamento de vértices de software totalmente em destaque (incluindo suporte para sombreadores de vértices personalizados). No entanto, nenhuma emulação é fornecida para operações em nível de pixel; os aplicativos devem verificar os bits de Caps apropriados e usar a API ValidateDevice para determinar o suporte.

</dd> <dt>

<span id="Is_there_a_software_rasterizer_included_with_Direct3D__"></span><span id="is_there_a_software_rasterizer_included_with_direct3d__"></span><span id="IS_THERE_A_SOFTWARE_RASTERIZER_INCLUDED_WITH_DIRECT3D__"></span>**Há um rasterizador de software incluído com o Direct3D?** 
</dt> <dd>

Não para aplicativos de desempenho. Um rasterizador de referência é fornecido para validação de driver, mas a implementação é projetada para precisão e não para desempenho. O Direct3D oferece suporte a rasterizadores de software de plug-in.

</dd> <dt>

<span id="How_can_I_perform_color_keying_with_DirectX_graphics__"></span><span id="how_can_i_perform_color_keying_with_directx_graphics__"></span><span id="HOW_CAN_I_PERFORM_COLOR_KEYING_WITH_DIRECTX_GRAPHICS__"></span>**Como posso executar a criação de cores com elementos gráficos do DirectX?** 
</dt> <dd>

Não há suporte direto para a codificação de cores. em vez disso, você precisará usar a mistura alfa para emular a chave de cores. A função D3DXCreateTextureFromFileEx () pode ser usada para facilitar isso. Essa função aceita um parâmetro de cor de chave e substituirá todos os pixels da imagem de origem que contém a cor especificada com pixels pretos transparentes na textura criada.

</dd> <dt>

<span id="Does_the_Direct3D_geometry_code_utilize_3DNow__and_or_Pentium_III_SIMD_instructions__"></span><span id="does_the_direct3d_geometry_code_utilize_3dnow__and_or_pentium_iii_simd_instructions__"></span><span id="DOES_THE_DIRECT3D_GEOMETRY_CODE_UTILIZE_3DNOW__AND_OR_PENTIUM_III_SIMD_INSTRUCTIONS__"></span>**O código de geometria do Direct3D utiliza as instruções 3DNow! e/ou Pentium III SIMD?** 
</dt> <dd>

Sim. O pipeline Direct3D Geometry tem vários caminhos de código diferentes, dependendo do tipo de processador, e ele utilizará as operações especiais de ponto flutuante fornecidas pelo 3DNow! ou as instruções de Pentium III SIMD em que estão disponíveis. Isso inclui o processamento de sombreadores de vértices personalizados.

</dd> <dt>

<span id="How_do_I_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="how_do_i_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="HOW_DO_I_PREVENT_TRANSPARENT_PIXELS_BEING_WRITTEN_TO_THE_Z-BUFFER__"></span>**Como fazer impedir que os pixels transparentes sejam gravados no buffer z?** 
</dt> <dd>

Você pode filtrar os pixels com um valor alfa acima ou abaixo de um determinado limite. Você controla esse comportamento usando renderstates ALPHATESTENABLE, ALPHAREF e ALPHAFUNC.

</dd> <dt>

<span id="What_is_a_stencil_buffer__"></span><span id="what_is_a_stencil_buffer__"></span><span id="WHAT_IS_A_STENCIL_BUFFER__"></span>**O que é um buffer de estêncil?** 
</dt> <dd>

Um buffer de estêncil é um buffer adicional de informações por pixel, assim como um buffer z. Na verdade, ele reside em alguns dos bits de um buffer z. Os formatos comum de estêncil/buffer z são um estêncil de 15 bits z e 1 bits ou um estêncil de 24 bits z e 8 bits. É possível executar operações aritméticas simples no conteúdo do buffer de estêncil por pixel, pois os polígonos são renderizados. Por exemplo, o buffer de estêncil pode ser incrementado ou diminuído, ou o pixel pode ser rejeitado se o valor do estêncil falhar em um teste de comparação simples. Isso é útil para efeitos que envolvem a marcação de uma região do buffer de quadro e a execução da renderização apenas da região marcada (ou desmarcada). Bons exemplos são efeitos volumétricoss, como volumes de sombra.

</dd> <dt>

<span id="How_do_I_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="how_do_i_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="HOW_DO_I_USE_A_STENCIL_BUFFER_TO_RENDER_SHADOW_VOLUMES__"></span>**Como fazer usar um buffer de estêncil para renderizar volumes de sombra?** 
</dt> <dd>

A chave para esse e outros efeitos de buffer de estêncil volumétricos é a interação entre o buffer de estêncil e o z-buffer. Uma cena com um volume de sombra é renderizada em três estágios. Primeiro, a cena sem a sombra é renderizada como de costume, usando o z-buffer. Em seguida, a sombra é marcada no buffer do estêncil da seguinte maneira. As faces frontais do volume de sombra são desenhadas usando polígonos invisíveis, com teste de z habilitado, mas z-gravações desabilitadas e o buffer de estêncil incrementado a cada pixel passando o teste z. As faces posteriores do volume de sombra são renderizadas da mesma forma, mas decrementando o valor do estêncil em vez disso.

Agora, considere um único pixel. Supondo que a câmera não esteja no volume de sombra, há quatro possibilidades para o ponto correspondente na cena. Se o raio da câmera até o ponto não interceptar o volume de sombra, nenhum polígono de sombra terá sido desenhado lá e o buffer de estêncil ainda será zero. Caso contrário, se o ponto estiver na frente do volume de sombra, os polígonos de sombra serão armazenados em buffer z e o estêncil novamente permanecerá inalterado. Se os pontos estiverem atrás do volume de sombra, o mesmo número de faces de sombra frontal como faces traseiras terá sido renderizado e o estêncil será zero, tendo sido incrementado quantas vezes forem decrementadas.

A possibilidade final é que o ponto está dentro do volume de sombra. Nesse caso, o verso do volume de sombra será armazenado em buffer z, mas não na face frontal, portanto, o buffer de estêncil será um valor diferente de zero. O resultado é que partes do buffer de quadro com base em sombra têm um valor de estêncil diferente de zero. Por fim, para realmente renderizar a sombra, toda a cena é desbotada com um polígono combinado alfa definido para afetar apenas os pixels com um valor de estêncil diferente de zero. Um exemplo dessa técnica pode ser visto no exemplo de "volume de sombra" que vem com o SDK do DirectX.

</dd> <dt>

<span id="What_are_the_texel_alignment_rules__How_do_I_get_a_one-to-one_mapping__"></span><span id="what_are_the_texel_alignment_rules__how_do_i_get_a_one-to-one_mapping__"></span><span id="WHAT_ARE_THE_TEXEL_ALIGNMENT_RULES__HOW_DO_I_GET_A_ONE-TO-ONE_MAPPING__"></span>**Quais são as regras de alinhamento do Texel? Como fazer obter um mapeamento um-para-um?** 
</dt> <dd>

Isso é explicado totalmente na documentação do Direct3D 9. No entanto, o resumo executivo é que você deve inclinar suas coordenadas de tela de-0,5 de um pixel para se alinhar corretamente com o texels. A maioria dos cartões agora está em conformidade com as regras de alinhamento Texel, no entanto, há alguns cartões ou drivers mais antigos que não têm. Para lidar com esses casos, o melhor conselho é entrar em contato com o fornecedor de hardware em questão e solicitar drivers atualizados ou sua solução alternativa sugerida. Observe que, no Direct3D 10, essa regra não é mais segura.

</dd> <dt>

<span id="What_is_the_purpose_of_the_D3DCREATE_PUREDEVICE_flag__"></span><span id="what_is_the_purpose_of_the_d3dcreate_puredevice_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_D3DCREATE_PUREDEVICE_FLAG__"></span>**Qual é a finalidade do sinalizador D3DCREATE \_ PUREDEVICE?** 
</dt> <dd>

Use o \_ sinalizador D3DCREATE PUREDEVICE durante a criação do dispositivo para criar um dispositivo puro. Um dispositivo puro não salva o estado atual (durante as alterações de estado), o que geralmente melhora o desempenho; Esse dispositivo também requer o processamento de vértices de hardware. Um dispositivo puro normalmente é usado quando o desenvolvimento e a depuração são concluídos e você deseja obter o melhor desempenho.

Uma desvantagem de um dispositivo puro é que ele não dá suporte a todas as \* chamadas get API; isso significa que você não pode usar um dispositivo puro para consultar o estado do pipeline. Isso dificulta a depuração durante a execução de um aplicativo. Abaixo está uma lista de todos os métodos que são desabilitados por um dispositivo puro.

-   [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane)
-   [**IDirect3DDevice9::GetClipStatus**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus)
-   [**IDirect3DDevice9:: GetLight**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight)
-   [**IDirect3DDevice9:: getclareable**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable)
-   [**IDirect3DDevice9:: GetMaterial**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial)
-   [**IDirect3DDevice9::GetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf)
-   [**IDirect3DDevice9::GetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti)
-   [**IDirect3DDevice9::GetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb)
-   [**IDirect3DDevice9:: getrenderingstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate)
-   [**IDirect3DDevice9:: getsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate)
-   [**IDirect3DDevice9::GetTextureStageState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate)
-   [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform)
-   [**IDirect3DDevice9::GetVertexShaderConstantF**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf)
-   [**IDirect3DDevice9::GetVertexShaderConstantI**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti)
-   [**IDirect3DDevice9::GetVertexShaderConstantB**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb)

Uma segunda desvantagem de um dispositivo puro é que ele não filtra nenhuma alteração de estado redundante. Ao usar um dispositivo puro, seu aplicativo deve reduzir o número de alterações de estado no loop de renderização para um mínimo; Isso pode incluir a filtragem de alterações de estado para garantir que os Estados não sejam definidos mais de uma vez. Essa desvantagem é dependente do aplicativo; Se você usar mais de uma chamada de conjunto de 1000 por quadro, considere aproveitar a filtragem de redundância feita automaticamente por um dispositivo não puro.

Assim como ocorre com todos os problemas de desempenho, a única maneira de saber se seu aplicativo será executado melhor com um dispositivo puro é comparar o desempenho do aplicativo com um dispositivo puro vs. não puro. Um dispositivo puro tem o potencial de acelerar um aplicativo reduzindo a sobrecarga da CPU da API. Mas tenha cuidado! Para alguns cenários, um dispositivo puro tornará o seu aplicativo mais lento (devido ao trabalho adicional de CPU causado por alterações de estado redundantes). Se você não tiver certeza de qual tipo de dispositivo funcionará melhor para seu aplicativo e não filtrar alterações redundantes no aplicativo, use um dispositivo não puro.

</dd> <dt>

<span id="How_do_I_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="how_do_i_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="HOW_DO_I_ENUMERATE_THE_DISPLAY_DEVICES_IN_A_MULTI-MONITOR_SYSTEM__"></span>**Como fazer enumerar os dispositivos de vídeo em um sistema de vários monitores?** 
</dt> <dd>

A enumeração pode ser executada por meio de uma iteração simples pelo aplicativo usando métodos da interface IDirect3D9. Chame GetAdapterCount para determinar o número de adaptadores de vídeo no sistema. Chame GetAdapterMonitor para determinar a qual monitor físico um adaptador está conectado (esse método retorna um HMONITOR, que você pode usar na API do Win32 GetMonitorInfo para determinar informações sobre o monitor físico). Determinar as características de um adaptador de vídeo específico ou criar um dispositivo Direct3D nesse adaptador é tão simples quanto passar o número do adaptador apropriado no lugar do \_ padrão D3DADAPTER ao chamar GetDeviceCaps, CreateDevice ou outros métodos.

</dd> <dt>

<span id="What_happened_to_Fixed_Function_Bumpmapping_in_D3D9__"></span><span id="what_happened_to_fixed_function_bumpmapping_in_d3d9__"></span><span id="WHAT_HAPPENED_TO_FIXED_FUNCTION_BUMPMAPPING_IN_D3D9__"></span>**O que aconteceu com a função fixa Bumpmapping em D3D9?** 
</dt> <dd>

A partir do Direct3D 9, fortalecemos a validação em cartões que podiam dar suporte apenas a > duas texturas simultâneas. Determinados cartões mais antigos têm apenas 3 estágios de textura disponíveis quando você usa uma operação alfa modular específica. O uso mais comum que as pessoas usam os três estágios para o é o bumpmapping de entalhe, e você ainda pode fazer isso com o D3D9.

O campo altura deve ser armazenado no canal alfa e é usado para modular a contribuição de luzes, isto é:

``` syntax
// Stage 0 is the base texture, with the height map in the alpha channel
m_pd3dDevice->SetTexture(0, m_pEmbossTexture );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 0 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP,   D3DTOP_MODULATE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP,   D3DTOP_SELECTARG1 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE );
if( m_bShowEmbossMethod )
{
 // Stage 1 passes through the RGB channels (SELECTARG2 = CURRENT), and 
 // does a signed add with the inverted alpha channel. 
 // The texture coords associated with Stage 1 are the shifted ones, so 
 // the result is:
 //    (height - shifted_height) * tex.RGB * diffuse.RGB
   m_pd3dDevice->SetTexture( 1, m_pEmbossTexture );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_SELECTARG2 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAOP, D3DTOP_ADDSIGNED );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG1, D3DTA_TEXTURE|D3DTA_COMPLEMENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG2, D3DTA_CURRENT );

   // Set up the alpha blender to multiply the alpha channel 
   // (monochrome emboss) with the src color (lighted texture)
   m_pd3dDevice->SetRenderState( D3DRS_ALPHABLENDENABLE, TRUE );
   m_pd3dDevice->SetRenderState( D3DRS_SRCBLEND,  D3DBLEND_SRCALPHA );
   m_pd3dDevice->SetRenderState( D3DRS_DESTBLEND, D3DBLEND_ZERO );
}
```

Este exemplo, juntamente com outros exemplos mais antigos, não são mais fornecidos na versão atual do SDK e não serão enviados em futuras versões do SDK.

</dd> </dl>

### <a name="geometry-vertex-processing"></a>Processamento de geometria (vértice)

<dl> <dt>

<span id="Vertex_streams_confuse_me_how_do_they_work__"></span><span id="vertex_streams_confuse_me_how_do_they_work__"></span><span id="VERTEX_STREAMS_CONFUSE_ME_HOW_DO_THEY_WORK__"></span>**Os fluxos de vértice confundem como funcionam?** 
</dt> <dd>

O Direct3D monta cada vértice que é colocado na parte de processamento do pipeline de um ou mais fluxos de vértice. Ter apenas um fluxo de vértice corresponde ao antigo modelo anterior ao DirectX 8, no qual os vértices são provenientes de uma única fonte. Com o DirectX 8, diferentes componentes de vértice podem vir de fontes diferentes; por exemplo, um buffer de vértice pode conter posições e normais, enquanto um segundo valores de cor e coordenadas de textura são mantidos.

</dd> <dt>

<span id="What_is_a_vertex_shader__"></span><span id="what_is_a_vertex_shader__"></span><span id="WHAT_IS_A_VERTEX_SHADER__"></span>**O que é um sombreador de vértice?** 
</dt> <dd>

Um sombreador de vértice é um procedimento para processar um único vértice. Ele é definido usando uma linguagem simples semelhante a assembly, que é montada pela biblioteca do utilitário D3DX em um fluxo de token que o Direct3D aceita. O sombreador de vértice usa como entrada um único vértice e um conjunto de valores constantes; Ele gera uma posição de vértice (no espaço de clipe) e, opcionalmente, um conjunto de cores e coordenadas de textura, que são usadas na rasterização. Observe que, quando você tem um sombreador de vértice personalizado, os componentes de vértice não têm mais nenhuma semântica aplicada a eles pelo Direct3D e os vértices são simplesmente dados arbitrários que são interpretados pelo sombreador de vértice que você criar.

</dd> <dt>

<span id="Does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="DOES_A_VERTEX_SHADER_PERFORM_PERSPECTIVE_DIVISION_OR_CLIPPING__"></span>**Um sombreador de vértice executa divisão em perspectiva ou recorte?** 
</dt> <dd>

Não. O sombreador de vértice gera uma coordenada homogênea no espaço de clipe para a posição de vértice transformada. A divisão de perspectiva e o recorte são executados automaticamente após o sombreador.

</dd> <dt>

<span id="Can_I_generate_geometry_with_a_vertex_shader__"></span><span id="can_i_generate_geometry_with_a_vertex_shader__"></span><span id="CAN_I_GENERATE_GEOMETRY_WITH_A_VERTEX_SHADER__"></span>**Posso gerar Geometry com um sombreador de vértice?** 
</dt> <dd>

Um sombreador de vértice não pode criar ou destruir vértices; Ele opera em um único vértice de cada vez, fazendo um vértice não processado como entrada e gerando um único vértice processado. Portanto, ele pode ser usado para manipular a geometria existente (aplicando as deformações ou realizando operações de aparência), mas não pode realmente gerar uma nova geometria por si.

</dd> <dt>

<span id="Can_I_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="can_i_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="CAN_I_APPLY_A_CUSTOM_VERTEX_SHADER_TO_THE_RESULTS_OF_THE_FIXED-FUNCTION_GEOMETRY_PIPELINE__OR_VICE-VERSA___"></span>**Posso aplicar um sombreador de vértice personalizado aos resultados do pipeline de geometria de função fixa (ou vice-versa)?** 
</dt> <dd>

Não. Você precisa escolher uma ou outra. Se você estiver usando um sombreador de vértice personalizado, você será responsável por executar toda a transformação de vértice.

</dd> <dt>

<span id="Can_I_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="can_i_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="CAN_I_USE_A_CUSTOM_VERTEX_SHADER_IF_MY_HARDWARE_DOES_NOT_SUPPORT_IT__"></span>**Posso usar um sombreador de vértice personalizado se meu hardware não oferecer suporte a ele?** 
</dt> <dd>

Sim. O mecanismo de processamento de vértices de software do Direct3D dá suporte total a sombreadores de vértices personalizados com um nível surpreendentemente alto de desempenho.

</dd> <dt>

<span id="How_do_I_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="how_do_i_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="HOW_DO_I_DETERMINE_IF_THE_HARDWARE_SUPPORTS_MY_CUSTOM_VERTEX_SHADER__"></span>**Como fazer determinar se o hardware dá suporte ao meu sombreador de vértice personalizado?** 
</dt> <dd>

Dispositivos capazes de dar suporte a sombreadores de vértice no hardware são necessários para preencher o campo D3DCAPS9:: VertexShaderVersion para indicar o nível de versão do sombreador de vértice ao qual eles dão suporte. Qualquer dispositivo que diz dar suporte a um nível específico de sombreador de vértice deve dar suporte a todos os sombreadores de vértices legais que atendem à especificação para esse nível ou abaixo.

</dd> <dt>

<span id="How_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="how_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="HOW_MANY_CONSTANT_REGISTERS_ARE_AVAILABLE_FOR_VERTEX_SHADERS__"></span>**Quantos registros constantes estão disponíveis para sombreadores de vértice?** 
</dt> <dd>

Os dispositivos com suporte a sombreadores de vértice vs 1,0 são necessários para dar suporte a um mínimo de registros de constante 96. Os dispositivos podem dar suporte a mais do que esse número mínimo e podem relatá-lo por meio do campo D3DCAPS9:: MaxVertexShaderConst.

</dd> <dt>

<span id="Can_I_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="can_i_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="CAN_I_SHARE_POSITION_DATA_BETWEEN_VERTICES_WITH_DIFFERENT_TEXTURE_COORDINATES__"></span>**Posso compartilhar dados de posição entre vértices com diferentes coordenadas de textura?** 
</dt> <dd>

O exemplo comum dessa situação é um cubo no qual você deseja usar uma textura diferente para cada face. Infelizmente, a resposta é não, atualmente, não é possível indexar os componentes de vértice de forma independente. Mesmo com vários fluxos de vértice, todos os fluxos são indexados juntos.

</dd> <dt>

<span id="When_I_submit_an_indexed_list_of_primitives__does_Direct3D_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_I_indexed__"></span><span id="when_i_submit_an_indexed_list_of_primitives__does_direct3d_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_i_indexed__"></span><span id="WHEN_I_SUBMIT_AN_INDEXED_LIST_OF_PRIMITIVES__DOES_DIRECT3D_PROCESS_ALL_OF_THE_VERTICES_IN_THE_BUFFER__OR_JUST_THE_ONES_I_INDEXED__"></span>**Quando eu envio uma lista indexada de primitivos, o Direct3D processa todos os vértices no buffer ou apenas aqueles que indexei?** 
</dt> <dd>

Ao usar o pipeline de geometria de software, o Direct3D primeiro transforma todos os vértices no intervalo que você enviou, em vez de transformá-los "sob demanda" conforme eles são indexados. Para dados compactados de forma densa (ou seja, onde a maioria dos vértices são usados), isso é mais eficiente, especialmente quando há instruções SIMD disponíveis. Se seus dados forem empacotados de forma grosseira (ou seja, vários vértices não são usados), talvez você queira considerar a reorganização dos dados para evitar muitas transformações redundantes. Ao usar a aceleração de geometria de hardware, os vértices são normalmente transformados sob demanda conforme são necessários.

</dd> <dt>

<span id="What_is_an_index_buffer__"></span><span id="what_is_an_index_buffer__"></span><span id="WHAT_IS_AN_INDEX_BUFFER__"></span>**O que é um buffer de índice?** 
</dt> <dd>

Um buffer de índice é exatamente análogo a um buffer de vértice, mas, em vez disso, ele contém índices para uso em chamadas DrawIndexedPrimitive. É altamente recomendável que você use buffers de índice em vez de memória bruta alocada por aplicativo, quando possível, pelos mesmos motivos que os buffers de vértice.

</dd> <dt>

<span id="I_notice_that_32-bit_indices_are_a_supported_type__can_I_use_them_on_all_devices__"></span><span id="i_notice_that_32-bit_indices_are_a_supported_type__can_i_use_them_on_all_devices__"></span><span id="I_NOTICE_THAT_32-BIT_INDICES_ARE_A_SUPPORTED_TYPE__CAN_I_USE_THEM_ON_ALL_DEVICES__"></span>**Observe que os índices de 32 bits são um tipo com suporte; Posso usá-los em todos os dispositivos?** 
</dt> <dd>

Não. Você deve verificar o campo D3DCAPS9:: MaxVertexIndex para determinar o valor de índice máximo que é suportado pelo dispositivo. Esse valor deve ser maior do que 2 para a 16º potência-1 (0xFFFF) para que haja suporte para buffers de índice do tipo D3DFMT \_ INDEX32. Além disso, observe que alguns dispositivos podem dar suporte a índices de 32 bits, mas dão suporte a um valor de índice máximo menor que 2 para o 32 º Power-1 (0xFFFFFFFF); Nesse caso, o aplicativo deve respeitar o limite relatado pelo dispositivo.

</dd> <dt>

<span id="Does_S_W_vertex_processing_support_64_bit__"></span><span id="does_s_w_vertex_processing_support_64_bit__"></span><span id="DOES_S_W_VERTEX_PROCESSING_SUPPORT_64_BIT__"></span>**O processamento de vértices S/W dá suporte a 64 bits?** 
</dt> <dd>

Há um pipeline de vértice s/w otimizado para x64, mas ele não existe para IA64.

</dd> </dl>

### <a name="performance-tuning"></a>Ajuste de desempenho

<dl> <dt>

<span id="How_can_I_improve_the_performance_of_my_Direct3D_application__"></span><span id="how_can_i_improve_the_performance_of_my_direct3d_application__"></span><span id="HOW_CAN_I_IMPROVE_THE_PERFORMANCE_OF_MY_DIRECT3D_APPLICATION__"></span>**Como posso melhorar o desempenho do meu aplicativo do Direct3D?** 
</dt> <dd>

Veja a seguir as principais áreas a serem examinadas ao otimizar o desempenho:

<dl> <dt>

<span id="Batch_size_"></span><span id="batch_size_"></span><span id="BATCH_SIZE_"></span>**Tamanho do lote** 
</dt> <dd>

O Direct3D é otimizado para grandes lotes de primitivos. Quanto mais polígonos podem ser enviados em uma única chamada, melhor. Uma boa regra prática é visar a média de 1000 vértices por chamada primitiva. Abaixo desse nível, você provavelmente não está obtendo um desempenho ideal, acima disso, e está em redução de retornos e conflitos potenciais com considerações de simultaneidade (veja abaixo).

</dd> <dt>

<span id="State_changes_"></span><span id="state_changes_"></span><span id="STATE_CHANGES_"></span>**Alterações de estado** 
</dt> <dd>

Alterar o estado de renderização pode ser uma operação cara, especialmente ao alterar a textura. Por esse motivo, é importante minimizar o máximo possível do número de alterações de estado feitas por quadro. Além disso, tente minimizar as alterações de vértice ou buffer de índice.

> [!Note]  
> A partir do DirectX 8, o custo da alteração do buffer de vértice não é mais tão caro quanto era com versões anteriores, mas ainda é uma prática recomendada evitar alterações no buffer de vértice sempre que possível.

 

</dd> <dt>

<span id="Concurrency"></span><span id="concurrency"></span><span id="CONCURRENCY"></span>**Corrente**
</dt> <dd>

Se você puder se organizar para executar a renderização simultaneamente com outro processamento, você aproveitará ao máximo o desempenho do sistema. Essa meta pode entrar em conflito com a meta de reduzir as alterações de renderingstate. Você precisa ter um equilíbrio entre o envio em lote para reduzir as alterações de estado e enviar dados por push para o driver antes para ajudar a alcançar a simultaneidade. O uso de vários buffers de vértices no modo Round Robin pode ajudar com a simultaneidade.

</dd> <dt>

<span id="Texture_uploads_"></span><span id="texture_uploads_"></span><span id="TEXTURE_UPLOADS_"></span>**Carregamentos de textura** 
</dt> <dd>

O carregamento de texturas para o dispositivo consome largura de banda e causa uma competição de largura de banda com dados de vértice. Portanto, é importante não fazer a confirmação da memória de textura, o que forçaria o esquema de cache a carregar quantidades excessivas de texturas em cada quadro.

</dd> <dt>

<span id="Vertex_and_index_buffers_"></span><span id="vertex_and_index_buffers_"></span><span id="VERTEX_AND_INDEX_BUFFERS_"></span>**Buffers de vértice e de índice** 
</dt> <dd>

Você sempre deve usar os buffers de vértice e de índice, em vez de blocos simples de memória alocada do aplicativo. No mínimo, a semântica de bloqueio para o vértice e os buffers de índice pode evitar uma operação de cópia redundante. Com alguns drivers, o vértice ou o buffer de índice podem ser colocados em memória mais ideal (talvez na memória de vídeo ou AGP) para acesso pelo hardware.

</dd> <dt>

<span id="State_macro_blocks_"></span><span id="state_macro_blocks_"></span><span id="STATE_MACRO_BLOCKS_"></span>**Blocos de macro de estado** 
</dt> <dd>

Elas foram introduzidas no DirectX 7,0. Eles fornecem um mecanismo para gravar uma série de alterações de estado (incluindo as alterações de iluminação, material e matriz) em uma macro, que pode ser reproduzida por uma única chamada. Isso apresenta duas vantagens:

-   Você reduz a sobrecarga de chamada fazendo uma chamada em vez de muitos.
-   Um driver ciente pode pré-configurar e pré-compilar as alterações de estado, tornando muito mais rápido enviar para o hardware de gráficos.

As alterações de estado ainda podem ser caras, mas o uso de macros de estado pode ajudar a reduzir pelo menos um pouco do custo. Use apenas um único dispositivo Direct3D. Se você precisar renderizar para vários destinos, use SetRenderTarget. Se você estiver criando um aplicativo em janela com várias janelas 3D, use a API CreateAdditionalSwapChain. O tempo de execução é otimizado para um único dispositivo e há uma penalidade de velocidade considerável para usar vários dispositivos.

</dd> </dl> </dd> <dt>

<span id="Which_primitive_types__strips__fans__lists_and_so_on__should_I_use__"></span><span id="which_primitive_types__strips__fans__lists_and_so_on__should_i_use__"></span><span id="WHICH_PRIMITIVE_TYPES__STRIPS__FANS__LISTS_AND_SO_ON__SHOULD_I_USE__"></span>**Quais tipos primitivos (faixas, ventiladores, listas e assim por diante) devo usar?** 
</dt> <dd>

Muitas malhas encontradas em vértices de recursos de dados reais que são compartilhados por vários polígonos. Para maximizar o desempenho, é desejável reduzir a duplicação em vértices transformados e enviados pelo barramento para o dispositivo de renderização. É claro que o uso de listas de triângulo simples não realiza nenhum compartilhamento de vértice, o que o torna o método menos ideal. A escolha é, então, entre o uso de faixas e ventiladores, o que implica uma relação de conectividade específica entre polígonos e o uso de listas indexadas. Em que os dados naturalmente se enquadram em faixas e ventiladores, essas são as opções mais apropriadas, pois minimizam os dados enviados ao driver. No entanto, a decomposição de malhas em faixas e ventiladores geralmente resulta em um grande número de partes separadas, o que implica um grande número de chamadas DrawPrimitive. Por esse motivo, o método mais eficiente geralmente é usar uma única chamada DrawIndexedPrimitive com uma lista de triângulos. Uma vantagem adicional de usar uma lista indexada é que um benefício pode ser obtido mesmo quando triângulos consecutivos compartilham apenas um único vértice. Em resumo, se os dados estiverem naturalmente em grandes faixas ou fãs, use faixas ou ventiladores; caso contrário, use listas indexadas.

</dd> <dt>

<span id="How_do_you_determine_the_total_texture_memory_a_card_has__excluding_AGP_memory__"></span><span id="how_do_you_determine_the_total_texture_memory_a_card_has__excluding_agp_memory__"></span><span id="HOW_DO_YOU_DETERMINE_THE_TOTAL_TEXTURE_MEMORY_A_CARD_HAS__EXCLUDING_AGP_MEMORY__"></span>**Como determinar a memória de textura total que um cartão tem, excluindo a memória AGP?** 
</dt> <dd>

[**IDirect3DDevice9:: GetAvailableTextureMem**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem) retorna a memória total disponível, incluindo AGP. Alocar recursos com base em uma suposição da quantidade de memória de vídeo que você tem não é uma ótima ideia. Por exemplo, e se o cartão estiver sendo executado sob uma arquitetura de memória unificada (uma) ou puder compactar as texturas? Pode haver mais espaço disponível do que você pode ter imaginado. Você deve criar recursos e verificar se há erros de "memória insuficiente" e, em seguida, reduzir novamente as texturas. Por exemplo, você pode remover os principais níveis MIP de suas texturas.

</dd> <dt>

<span id="What_s_a_good_usage_pattern_for_vertex_buffers_if_I_m_generating_dynamic_data__"></span><span id="what_s_a_good_usage_pattern_for_vertex_buffers_if_i_m_generating_dynamic_data__"></span><span id="WHAT_S_A_GOOD_USAGE_PATTERN_FOR_VERTEX_BUFFERS_IF_I_M_GENERATING_DYNAMIC_DATA__"></span>**Qual é um bom padrão de uso para buffers de vértice se eu estiver gerando dados dinâmicos?** 
</dt> <dd>

1.  Crie um buffer de vértice usando os \_ sinalizadores de uso D3DUSAGE dinâmico e D3DUSAGE \_ WRITEONLY e o \_ sinalizador de pool padrão D3DPOOL. (Também especifique D3DUSAGE \_ SOFTWAREPROCESSING se você estiver usando o processamento de vértice de software.)
2.  I = 0.
3.  Definir estado (texturas, renderstates e assim por diante).
4.  Verificar se há espaço no buffer, ou seja, I + M <= N? (Onde M é o número de novos vértices).
5.  Em caso afirmativo, bloqueie o VB com D3DLOCK \_ NoOverwrite. Isso informa ao Direct3D e ao driver que você adicionará vértices e não modificará aqueles que você criou anteriormente em lote. Portanto, se uma operação de DMA estava em andamento, ela não será interrompida. Se não, goto 11.
6.  Preencha os vértices M em I.
7.  Automático.
8.  Chamar \[ primitiva indexada de desenho \] . Para primitivos não indexados, use I como o parâmetro StartVertex. Para primitivos indexados, certifique-se de que os índices apontam para a parte correta do buffer de vértice (pode ser mais fácil usar o parâmetro BaseVertexIndex da chamada SetIndices para conseguir isso).
9.  I + = M.
10. Ir para 3.
11. Ok, estamos sem espaço, então vamos começar com um novo VB. Não queremos usar o mesmo porque pode haver uma operação DMA em andamento. Podemos nos comunicar com o Direct3D e com o driver bloqueando o mesmo VB com o \_ sinalizador de descarte D3DLOCK. O que isso significa é "você pode me dar um novo ponteiro, pois estou pronto com o antigo e não se preocupe muito com o conteúdo antigo".
12. I = 0.
13. Goto 4 (ou 6).

</dd> <dt>

<span id="Why_do_I_have_to_specify_more_information_in_the_D3DVERTEXELEMENT9_structure__"></span><span id="why_do_i_have_to_specify_more_information_in_the_d3dvertexelement9_structure__"></span><span id="WHY_DO_I_HAVE_TO_SPECIFY_MORE_INFORMATION_IN_THE_D3DVERTEXELEMENT9_STRUCTURE__"></span>**Por que preciso especificar mais informações na estrutura D3DVERTEXELEMENT9?** 
</dt> <dd>

A partir do Direct3D 9, a declaração de fluxo de vértice não é mais apenas uma matriz DWORD, agora é uma matriz de estruturas D3DVERTEXELEMENT9. O tempo de execução usa as informações de uso e semântica adicionais para associar o conteúdo dos fluxos de vértice a entradas/registros de entrada de sombreadores de vértice. Para o Direct3D 9, as declarações de vértice são dissociadas de sombreadores de vértice, o que facilita o uso de sombreadores com geometrias de formatos diferentes, pois o tempo de execução só associa os dados necessários ao sombreador.

As novas declarações de vértice podem ser usadas com o pipeline de função fixa ou com sombreadores. Para o pipeline de função fixa, não é necessário chamar SetVertexShader. Se, no entanto, você quiser alternar para o pipeline de função fixa e tiver usado anteriormente um sombreador de vértice, chame SetVertexShader (NULL). Quando isso for feito, você ainda precisará chamar SetFVF para declarar o código FVF.

Ao usar sombreadores de vértice, chame SetVertexShader com o objeto de sombreador de vértice. Além disso, chame SetFVF para configurar uma declaração de vértice. Isso usa as informações implícitas no FVF. SetVertexDeclaration pode ser chamado no lugar de SetFVF porque oferece suporte a declarações de vértice que não podem ser expressas com um FVF.

</dd> </dl>

### <a name="d3dx-utility-library"></a>Biblioteca do utilitário D3DX

<dl> <dt>

<span id="What_file_formats_are_supported_by_the_D3DX_image_file_loader_functions__"></span><span id="what_file_formats_are_supported_by_the_d3dx_image_file_loader_functions__"></span><span id="WHAT_FILE_FORMATS_ARE_SUPPORTED_BY_THE_D3DX_IMAGE_FILE_LOADER_FUNCTIONS__"></span>**Quais formatos de arquivo são compatíveis com as funções do carregador de arquivo de imagem D3DX?** 
</dt> <dd>

As funções do carregador de arquivo de imagem D3DX dão suporte a arquivos BMP, TGA, JPG, DIB, PPM e DDS.

</dd> <dt>

<span id="The_text_rendering_functions_in_D3DX_don_t_seem_to_work__what_am_I_doing_wrong__"></span><span id="the_text_rendering_functions_in_d3dx_don_t_seem_to_work__what_am_i_doing_wrong__"></span><span id="THE_TEXT_RENDERING_FUNCTIONS_IN_D3DX_DON_T_SEEM_TO_WORK__WHAT_AM_I_DOING_WRONG__"></span>**As funções de renderização de texto no D3DX não parecem funcionar, o que estou fazendo errado?** 
</dt> <dd>

Um erro comum ao usar as funções ID3DXFont::D rawText é especificar um componente alfa zero para o parâmetro de cor; resultando em texto completamente transparente (ou seja, invisível). Para texto totalmente opaco, verifique se o componente alfa do parâmetro de cor está totalmente saturado (255).

</dd> <dt>

<span id="How_can_I_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="how_can_i_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="HOW_CAN_I_SAVE_THE_CONTENTS_OF_A_SURFACE_OR_TEXTURE_TO_A_FILE__"></span>**Como posso salvar o conteúdo de uma superfície ou textura em um arquivo?** 
</dt> <dd>

O SDK do DirectX 8,1 adicionou duas funções à biblioteca D3DX especificamente para essa finalidade: D3DXSaveSurfaceToFile () e D3DXSaveTextureToFile (). Essas funções dão suporte à gravação de uma imagem em um arquivo no formato BMP ou DDS. Em versões anteriores, você terá que bloquear a superfície e ler os dados da imagem e, em seguida, gravá-los em um arquivo de bitmap. Para obter informações sobre como escrever uma função para armazenar bitmaps, consulte [armazenando uma imagem](/windows/desktop/gdi/storing-an-image).

Como alternativa, o GDI+ poderia ser usado para salvar a imagem em uma ampla variedade de formatos, embora isso exija que arquivos de suporte adicionais sejam distribuídos com seu aplicativo.

</dd> <dt>

<span id="How_can_I_make_use_of_the_High_Level_Shader_Language__HLSL__in_my_game__"></span><span id="how_can_i_make_use_of_the_high_level_shader_language__hlsl__in_my_game__"></span><span id="HOW_CAN_I_MAKE_USE_OF_THE_HIGH_LEVEL_SHADER_LANGUAGE__HLSL__IN_MY_GAME__"></span>**Como fazer para usar o HLSL (linguagem de sombreamento de alto nível) em meu jogo?** 
</dt> <dd>

Há três maneiras de incorporar a HLSL (linguagem de sombreamento de alto nível) da Microsoft ao seu mecanismo de jogo:

-   Compile a origem do sombreador em um assembly de sombreamento de vértice ou de pixel (usando o utilitário de linha de comando fxc.exe) e use D3DXAssembleShader () em tempo de execução. Dessa forma, até mesmo um jogo DirectX 8 pode tirar proveito do poder do HLSL.
-   Use D3DXCompileShader () para compilar a origem do sombreador no fluxo do token e no formulário da tabela de constantes. Em tempo de execução, carregue o fluxo de token e a tabela de constantes e chame CreateVertexShader () ou CreatePixelShader () no dispositivo para criar os sombreadores.
-   A maneira mais fácil de colocar em funcionamento é tirar proveito do sistema de efeitos D3DX chamando D3DXCreateEffectFromFile () ou D3DXCreateEffectFromResource () com o arquivo de efeito.

</dd> <dt>

<span id="What_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="what_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_NEW_SHADER_COMPILER_FLAG__"></span>**Qual é a finalidade do novo sinalizador do compilador do sombreador?** 
</dt> <dd>

A partir do SDK do DirectX de dezembro de 2006, o novo compilador HLSL desenvolvido para o Direct3D 10 foi habilitado para destinos do Direct3D 9. O novo compilador não tem suporte para \_ destinos PS 1 \_ x e agora é o compilador padrão para todos os sombreadores do Direct3D HLSL. Um sinalizador para compatibilidade com versões anteriores pode ser usado para forçar \_ destinos PS 1 \_ x a compilar como \_ destinos PS 2 \_ 0.

Os aplicativos que desejam usar o compilador herdado podem continuar a fazer isso fornecendo um sinalizador no tempo de execução (consulte os [**sinalizadores do compilador**](/windows/desktop/direct3d9/d3dxshader-flags)) ou fornecendo uma opção ao usar FXC.

</dd> <dt>

<span id="What_is_the_correct_way_to_get_shaders_from_an_Effect__"></span><span id="what_is_the_correct_way_to_get_shaders_from_an_effect__"></span><span id="WHAT_IS_THE_CORRECT_WAY_TO_GET_SHADERS_FROM_AN_EFFECT__"></span>**Qual é a maneira correta de obter sombreadores de um efeito?** 
</dt> <dd>

Use D3DXCreateEffect para criar um ID3DXEffect e, em seguida, use GetPassDesc para recuperar um D3DXPASS \_ desc. Esta estrutura contém ponteiros para os sombreadores de vértices e de pixel.

Não use ID3DXEffectCompiler:: GetPassDesc. Os identificadores de sombreador de vértice e de pixel retornados deste método são nulos.

</dd> <dt>

<span id="What_is_the_HLSL_noise___intrinsic_for__"></span><span id="what_is_the_hlsl_noise___intrinsic_for__"></span><span id="WHAT_IS_THE_HLSL_NOISE___INTRINSIC_FOR__"></span>**O que é o HLSL Noise () intrínseco para?** 
</dt> <dd>

A função intrínseca de ruído gera o ruído de Perl, conforme definido por Ken Perl. Atualmente, a função HLSL pode ser usada apenas para preencher texturas em sombreadores de textura, pois a h/w atual não oferece suporte ao método nativamente. Os sombreadores de textura são usados em juntamente com as \* funções de textura D3DXFill () que são funções auxiliares úteis para gerar texturas definidas de procedimento durante o tempo de carregamento.

</dd> <dt>

<span id="How_do_I_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="how_do_i_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="HOW_DO_I_DETECT_WHETHER_TO_USE_PIXEL_SHADER_MODEL_2.0_OR_2.A__"></span>**Como fazer detectar se o modelo de sombreador de pixel 2,0 ou 2 deve ser usado?** 
</dt> <dd>

Você pode usar as funções D3DXGetPixelShaderProfile () e D3DXGetPixelShaderProfile () que retornam uma cadeia de caracteres que determina qual perfil de HLSL é mais adequado para o dispositivo que está sendo executado.

</dd> <dt>

<span id="How_do_I_access_the_Parameters_in_my_Precompiled_Effects_Shaders__"></span><span id="how_do_i_access_the_parameters_in_my_precompiled_effects_shaders__"></span><span id="HOW_DO_I_ACCESS_THE_PARAMETERS_IN_MY_PRECOMPILED_EFFECTS_SHADERS__"></span>**Como fazer acessar os parâmetros em meus sombreadores de efeitos pré-compilados?** 
</dt> <dd>

Por meio da interface ID3DXConstantTable, que é usada para acessar a tabela de constantes. Esta tabela contém as variáveis que são usadas por sombreadores e efeitos de linguagem de alto nível.

</dd> <dt>

<span id="Is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="IS_THERE_A_WAY_TO_ADD_USER_DATA_TO_AN_EFFECT_OR_OTHER_RESOURCE__"></span>**Há uma maneira de adicionar dados de usuário a um efeito ou a outro recurso?** 
</dt> <dd>

Sim, para definir dados privados, você chama SetPrivateData (pReal é o objeto de textura do D3D, pSpoof é o objeto de textura encapsulado).

``` syntax
hr = pReal->SetPrivateData(IID_Spoof, &pSpoof, 
            sizeof(IDirect3DResource9*), 0)));
```

Para pesquisar o ponteiro encapsulado:

``` syntax
    IDirect3DResource9* pSpoof;
    DWORD dwSize = sizeof(pSpoof);
    hr = pReal->GetPrivateData(IID_Spoof, (void*) &pSpoof, &dwSize);
```

</dd> <dt>

<span id="Why_does_rendering_of_an_ID3DXMesh_object_slow_down_significantly_after_I_define_subsets__"></span><span id="why_does_rendering_of_an_id3dxmesh_object_slow_down_significantly_after_i_define_subsets__"></span><span id="WHY_DOES_RENDERING_OF_AN_ID3DXMESH_OBJECT_SLOW_DOWN_SIGNIFICANTLY_AFTER_I_DEFINE_SUBSETS__"></span>**Por que a renderização de um objeto ID3DXMesh diminui significativamente após eu definir os subconjuntos?** 
</dt> <dd>

Provavelmente, você não otimizou a malha depois de definir os atributos de face. Se você especificar atributos e, em seguida, chamar ID3DXMesh::D rawSubset (), esse método deverá executar uma pesquisa da malha para todas as faces que contêm os atributos solicitados. Além disso, as faces renderizadas provavelmente estão em um padrão de acesso aleatório, portanto, não utilizando o cache de vértice. Depois de definir os atributos de face para seus subconjuntos, chame os métodos ID3DXMesh:: Optimize ou ID3DXMesh:: OptimizeInPlace e especifique um método de otimização de D3DXMESHOPT \_ ATTRSORT ou mais forte. Observe que, para o desempenho ideal, você deve otimizar com o \_ sinalizador D3DXMESHOPT VERTEXCACHE, que também reordenará os vértices para a utilização de cache de vértice ideal. A matriz de adjacência gerada para uma malha D3DX tem três entradas por face, mas algumas faces podem não ter rostos adjacentes em todas as três bordas. Como isso é codificado? As entradas em que não há faces adjacentes são codificadas como 0xFFFFFFFF.

</dd> <dt>

<span id="I_ve_heard_a_lot_about_Pre-computed_Radiance_Transfer__PRT___where_can_I_learn_more__"></span><span id="i_ve_heard_a_lot_about_pre-computed_radiance_transfer__prt___where_can_i_learn_more__"></span><span id="I_VE_HEARD_A_LOT_ABOUT_PRE-COMPUTED_RADIANCE_TRANSFER__PRT___WHERE_CAN_I_LEARN_MORE__"></span>**Ouvi um grande número de PRT (transferência de radiante) previamente calculado, onde posso saber mais?** 
</dt> <dd>

O PRT é um novo recurso do D3DX adicionado na atualização do SDK do verão 2003. Ele permite a renderização de cenários de iluminação complexos, como global-llumination, sombreamento suave e dispersão de subsuperfície em tempo real. O SDK contém documentação e exemplos de como integrar a tecnologia ao seu jogo. Os exemplos de exemplo de demonstração de PRT e LocalDeformablePRT demonstram como usar o simulador para cenários de iluminação por vértice e por pixel, respectivamente. Mais informações sobre este e outros tópicos também podem ser encontradas na página da Web do Peter Pikes Sloan.

</dd> <dt>

<span id="How_can_I_render_to_a_texture_and_make_use_of_Anti_Aliasing__"></span><span id="how_can_i_render_to_a_texture_and_make_use_of_anti_aliasing__"></span><span id="HOW_CAN_I_RENDER_TO_A_TEXTURE_AND_MAKE_USE_OF_ANTI_ALIASING__"></span>**Como posso renderizar para uma textura e fazer uso da suavização de serrilhado?** 
</dt> <dd>

Crie um destino de renderização multiamostrado usando Direct3DDevice9:: CreateRenderTarget. Depois de renderizar a cena para esse destino de renderização, StretchRect a partir dela para uma textura de destino de renderização. Se você fizer alguma alteração para o textre fora da tela (como borrar ou cair dele), copie-o de volta para o buffer de fundo antes de apresentá-lo ().

</dd> </dl>

## <a name="directsound-questions"></a>Perguntas sobre o DirectSound

<dl> <dt>

<span id="Why_do_I_get_a_burst_of_static_when_my_application_starts_up__I_notice_this_problem_with_other_applications_too._"></span><span id="why_do_i_get_a_burst_of_static_when_my_application_starts_up__i_notice_this_problem_with_other_applications_too._"></span><span id="WHY_DO_I_GET_A_BURST_OF_STATIC_WHEN_MY_APPLICATION_STARTS_UP__I_NOTICE_THIS_PROBLEM_WITH_OTHER_APPLICATIONS_TOO._"></span>**Por que obtenho uma intermitência de estática quando meu aplicativo é iniciado? Eu observo esse problema também com outros aplicativos.** 
</dt> <dd>

Você provavelmente instalou o tempo de execução de depuração DirectX. A versão de depuração do tempo de execução preenche os buffers com estáticos para ajudar os desenvolvedores a detectar bugs com buffers não inicializados. Você não pode garantir o conteúdo de um buffer do DirectSound após a criação; em particular, você não pode supor que um buffer com seja zerado.

</dd> <dt>

<span id="Why_I_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="why_i_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="WHY_I_AM_EXPERIENCING_A_DELAY_IN_BETWEEN_CHANGING_AN_EFFECTS_PARAMETERS_AND_HEARING_THE_RESULTS__"></span>**Por que estou tendo um atraso entre alterar os parâmetros de efeitos e ouvir os resultados?** 
</dt> <dd>

As alterações nos parâmetros de efeito nem sempre ocorrem imediatamente no DirectX 8. Para eficiência, o DirectSound processa 100 milissegundos de dados de som em um buffer, iniciando no cursor de reprodução, antes de o buffer ser reproduzido. Esse pré-processamento ocorre após todas as seguintes chamadas:

``` syntax
IDirectSoundBuffer8::SetCurrentPosition
IDirectSoundBuffer8::SetFX
IDirectSoundBuffer8::Stop
IDirectSoundBuffer8::Unlock
```

A partir do DirectX 9, um novo algoritmo de processamento FX que processa os efeitos just-in-time resolve esse problema e reduziu a latência. O algoritmo foi adicionado à chamada IDirectSoundBuffer8::P deite (), juntamente com um thread adicional que processa os efeitos logo antes do cursor de gravação. Portanto, você pode definir parâmetros a qualquer momento e eles funcionarão conforme o esperado. No entanto, observe que em um buffer de reprodução haverá um pequeno atraso (geralmente 100 ms) antes de você ouvir a alteração do parâmetro, pois o áudio entre os cursores de reprodução e gravação (e um pouco mais de preenchimento) já foi processado nesse momento.

</dd> <dt>

<span id="How_do_I_detect_if_DSound_is_installed__"></span><span id="how_do_i_detect_if_dsound_is_installed__"></span><span id="HOW_DO_I_DETECT_IF_DSOUND_IS_INSTALLED__"></span>**Como fazer detectar se o DSound está instalado?** 
</dt> <dd>

Se você não precisar usar DirectSoundEnumerate () para listar os dispositivos DSound disponíveis, não vincule seu aplicativo com dsound. lib e, em vez disso, use-o por meio de COMs CoCreateInstance (CLSID \_ DirectSound...) e, em seguida, inicialize o objeto dsound usando Initialize (NULL). Se você precisar usar DirectSoundEnumerate (), poderá carregar dinamicamente dsound.dll usando LoadLibrary ("dsound.dll"); e acesse seus métodos usando GetProcAddress ("DirectSoundEnumerateA/W") e GetProcAddress ("DirectSoundCreateA/W") e assim por diante.

</dd> <dt>

<span id="How_do_I_create_multichannel_audio_with_WAVEFORMATEXTENSIBLE__"></span><span id="how_do_i_create_multichannel_audio_with_waveformatextensible__"></span><span id="HOW_DO_I_CREATE_MULTICHANNEL_AUDIO_WITH_WAVEFORMATEXTENSIBLE__"></span>**Como fazer criar áudio de multicanal com WAVEFORMATEXTENSIBLE?** 
</dt> <dd>

Se você não encontrar uma resposta à sua pergunta nos arquivos de ajuda do DirectSound, há um bom artigo com mais informações disponíveis em dados de áudio de vários canais e arquivos WAVE.

</dd> <dt>

<span id="How_can_I_use_the_DirectSound_Voice_Manager_with_property_sets_like_EAX__"></span><span id="how_can_i_use_the_directsound_voice_manager_with_property_sets_like_eax__"></span><span id="HOW_CAN_I_USE_THE_DIRECTSOUND_VOICE_MANAGER_WITH_PROPERTY_SETS_LIKE_EAX__"></span>**Como posso usar o Gerenciador de voz do DirectSound com conjuntos de propriedades como o EAX?** 
</dt> <dd>

No DirectSound 9,0, quando você duplica um buffer, agora é possível obter a interface IDirectSoundBuffer8 no buffer duplicado, o que dará acesso ao método AcquireResources. Isso permitirá que você associe um buffer ao sinalizador DSBCAPS \_ LOCDEFER a um recurso de hardware. Em seguida, você pode definir seus parâmetros EAX nesse buffer antes de ter que chamar Play ().

</dd> <dt>

<span id="I_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._How_can_I_get_more_accurate_information__"></span><span id="i_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._how_can_i_get_more_accurate_information__"></span><span id="I_AM_HAVING_PROBLEMS_WITH_UNRELIABLE_BEHAVIOR_WHEN_USING_CURSOR_POSITION_NOTIFICATIONS._HOW_CAN_I_GET_MORE_ACCURATE_INFORMATION__"></span>**Estou tendo problemas com o comportamento não confiável ao usar notificações de posição do cursor. Como posso obter informações mais precisas?** 
</dt> <dd>

Há alguns bugs sutis em várias versões do DirectSound, a pilha de áudio principal do Windows e os drivers de áudio que tornam as notificações de posições de cursor não confiáveis. A menos que você esteja visando uma configuração conhecida de HW/SW em que você sabe que as notificações estão bem comparadas, evite as notificações de posição do cursor. Para o controle de posição GetCurrentPosition () é uma técnica mais segura.

</dd> <dt>

<span id="I_am_suffering_from_performance_degradation_when_using_GetCurrentPosition__._What_can_I_do_to_improve_performance__"></span><span id="i_am_suffering_from_performance_degradation_when_using_getcurrentposition__._what_can_i_do_to_improve_performance__"></span><span id="I_AM_SUFFERING_FROM_PERFORMANCE_DEGRADATION_WHEN_USING_GETCURRENTPOSITION__._WHAT_CAN_I_DO_TO_IMPROVE_PERFORMANCE__"></span>**Estou sofrendo da degradação do desempenho ao usar GetCurrentPosition (). O que posso fazer para melhorar o desempenho?** 
</dt> <dd>

Cada chamada de GetCurrentPosition () em cada buffer causa uma chamada do sistema e as chamadas do sistema devem ser minimizadas, pois são um componente grande da superfície da CPU do DSound. No NT (Win2K e XP), os cursores em buffers de SW (e buffers de HW em alguns dispositivos) se movem em incrementos de 10 ms, de modo que chamar GetCurrentPosition () a cada 10 é ideal. Chamá-lo com mais frequência do que todos os 5 ms causará uma degradação do desempenho.

</dd> <dt>

<span id="My_DirectSound_application_is_taking_up_too_much_CPU_time_or_is_performing_slowly._Is_there_anything_I_can_do_to_optimize_my_code__"></span><span id="my_directsound_application_is_taking_up_too_much_cpu_time_or_is_performing_slowly._is_there_anything_i_can_do_to_optimize_my_code__"></span><span id="MY_DIRECTSOUND_APPLICATION_IS_TAKING_UP_TOO_MUCH_CPU_TIME_OR_IS_PERFORMING_SLOWLY._IS_THERE_ANYTHING_I_CAN_DO_TO_OPTIMIZE_MY_CODE__"></span>**Meu aplicativo DirectSound está ocupando muito tempo de CPU ou está sendo executado lentamente. Há algo que eu posso fazer para otimizar meu código?** 
</dt> <dd>

Há várias coisas que você pode fazer para melhorar o desempenho do seu código de áudio:

-   Não chame GetCurrentPosition com muita frequência. Cada chamada de GetCurrentPosition () em cada buffer causa uma chamada do sistema e as chamadas do sistema devem ser minimizadas, pois são um componente grande da superfície da CPU do DSound. No NT (Win2K e XP), os cursores em buffers de SW (e buffers de HW em alguns dispositivos) se movem em incrementos de 10 ms, de modo que chamar GetCurrentPosition () a cada 10 é ideal. Chamá-lo com mais frequência do que cada 5 ms causará uma degradação de desempenho.
-   Utilize uma taxa de quadros separada e menor para áudio. Hoje em dia, muitos jogos do Windows podem exceder 100 quadros por segundo e não é necessário na maioria dos casos para atualizar os parâmetros de áudio 3D na mesma taxa de quadros. O processamento de áudio a cada segundo ou terceiro quadro de gráficos, ou a cada 30ms, pode reduzir significativamente o número de chamadas de áudio em todo o aplicativo, sem reduzir a qualidade de áudio.
-   Use DS3D \_ adiado para objetos 3D. A maioria das placas de som responde imediatamente às alterações de parâmetros e em um único quadro pode ser alterada, especialmente se você alterar a posição ou a orientação do ouvinte. Isso faz com que o soundcard/CPU execute muitos cálculos desnecessários, portanto, outra otimização rápida e universal é adiar algumas alterações de parâmetro e confirmá-las no final do quadro.

    ou, pelo menos, use SetAllParameters em vez de chamadas individuais Set3DParamX em buffers.

    Da mesma forma, você deve usar pelo menos o uso de chamadas SetAllParamenters em buffers 3D em vez de chamadas Set3DParamX individuais. Basta tentar minimizar as chamadas do sistema sempre que possível.

-   Não faça chamadas redundantes; armazene e classifique uma lista de chamadas de reprodução. Geralmente, em um quadro de atualização de áudio, há duas solicitações para reproduzir novos sons. Se as solicitações forem processadas à medida que chegarem, o primeiro som novo poderá ser iniciado e, em seguida, substituído imediatamente o segundo som solicitado. Isso resulta em cálculos redundantes, uma chamada de reprodução desnecessária e uma chamada de parada desnecessária. É melhor armazenar uma lista de solicitações para que novos sons sejam reproduzidos, de modo que a lista possa ser classificada, e somente as vozes que devem começar a ser reproduzidas, na verdade já foram jogadas.

    Além disso, você deve armazenar cópias locais dos parâmetros 3D e EAX para cada fonte de som. Se for feita uma solicitação para definir um parâmetro para um valor específico, você poderá verificar se o valor é, na verdade, diferente do último conjunto de valores. Se não estiver, a chamada não precisará ser feita.

    Embora o driver da placa de som provavelmente detecte esse cenário e não execute o (mesmo) cálculo novamente, a chamada de áudio precisará alcançar o driver de áudio (por meio de uma transição de anel) e essa já é uma operação lenta.

</dd> <dt>

<span id="When_I_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._What_s_the_best_way_to_stream_a_buffer__"></span><span id="when_i_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._what_s_the_best_way_to_stream_a_buffer__"></span><span id="WHEN_I_STREAM_A_BUFFER_IT_TENDS_TO_GLITCH_AND_PERFORM_POORLY._WHAT_S_THE_BEST_WAY_TO_STREAM_A_BUFFER__"></span>**Quando faço o streaming de um buffer, ele tende a apresentar uma falha e é mal executado. Qual é a melhor maneira de transmitir um buffer?** 
</dt> <dd>

Ao transmitir áudio para um buffer, há dois algoritmos básicos: After-Write-cursor (AWC) e before-Play-cursor (BPC). O AWC minimiza a latência no custo da falha, enquanto BPC é o oposto. Como geralmente não há alterações interativas no som transmitido, esse tipo de latência raramente é um problema para jogos e aplicativos semelhantes, portanto, BPC é o algoritmo mais apropriado. No AWC, cada vez que seu thread de streaming executa "cima" dos dados em seus buffers de loop até N MS além dos cursores de gravação (normalmente N = 40 ou mais, para permitir a tremulação do agendamento do Windows). Em BPC, você sempre escreve tantos dados para os buffers quanto possível, preenchendo-os de acordo com os cursores de reprodução (ou talvez 32 bytes antes de permitir que os drivers relatem incorretamente o andamento do cursor de reprodução).

Use BPC para mimimize a falha e use buffers de 100 ms ou mais, mesmo que seus jogos não tenham problemas no seu hardware de teste, haverá uma falha em algum computador lá.

</dd> <dt>

<span id="I_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_Play___call_takes_a_long_time._What_should_I_do__"></span><span id="i_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_play___call_takes_a_long_time._what_should_i_do__"></span><span id="I_AM_PLAYING_THE_SAME_SOUNDS_OVER_AND_OVER_VERY_OFTEN_AND_VERY_QUICKLY_AND_SOMETIMES_THEY_DON_T_PLAY_PROPERLY__OR_THE_PLAY___CALL_TAKES_A_LONG_TIME._WHAT_SHOULD_I_DO__"></span>**Estou jogando os mesmos sons várias vezes e com muita frequência e, com algumas ocasiões, eles não são reproduzidos corretamente, ou a chamada Play () leva muito tempo. O que devo fazer?** 
</dt> <dd>

A latência de inicialização (que é diferente da latência de streaming mencionada acima) pode ser um problema no caso de algum hardware (a chamada Play () demora muito tempo em algumas placas de som. Se você realmente quiser reduzir essa latência, para sons twitchs (tomadas de pressão, trilha e assim por diante). um truque útil é manter alguns buffers sempre executando um loop e tocando em silêncio. Quando você precisar reproduzir um som Twitch, escolha um buffer livre, veja onde está o cursor de gravação e coloque o som no buffer apenas fora do cursor de gravação. Alguns soundcards falham QuerySupport para propriedades adiadas que eu sei que eles dão suporte. Há uma solução alternativa? Você poderia apenas QuerySupport as versões não adiadas das propriedades e usar as configurações adiadas de qualquer forma. Os drivers soundcard mais recentes também podem corrigir esse problema.

</dd> <dt>

<span id="How_do_I_encode_WAV_files_into_WMA__"></span><span id="how_do_i_encode_wav_files_into_wma__"></span><span id="HOW_DO_I_ENCODE_WAV_FILES_INTO_WMA__"></span>**Como fazer codificar arquivos WAV em WMA?** 
</dt> <dd>

Consulte a documentação no Windows Media Encoder em: Windows Media Encoder 9 Series.

</dd> <dt>

<span id="How_do_I_decode_MP3_files_with_DirectSound__"></span><span id="how_do_i_decode_mp3_files_with_directsound__"></span><span id="HOW_DO_I_DECODE_MP3_FILES_WITH_DIRECTSOUND__"></span>**Como fazer decodificar arquivos MP3 com DirectSound?** 
</dt> <dd>

O DirectSound não dá suporte nativo à decodificação de MP3. Você pode decodificar os arquivos com antecedência (usando um codec do ACM de um filtro do DirectShow) ou simplesmente usar o próprio DirectShow, o que pode fazer a decodificação para você; em seguida, você pode copiar os dados de áudio do PCM resultantes em seus buffers do DirectSound.

</dd> </dl>

## <a name="directx-extensions-for-alias-maya"></a>Extensões do DirectX para Alias Maya

<dl> <dt>

<span id="Why_aren_t_my_NURBS_showing_up__"></span><span id="why_aren_t_my_nurbs_showing_up__"></span><span id="WHY_AREN_T_MY_NURBS_SHOWING_UP__"></span>**Por que minha NURBS não está aparecendo?** 
</dt> <dd>

Não há suporte para NURBS. Você pode convertê-los em malhas de polígono.

</dd> <dt>

<span id="Why_aren_t_my_SUBDs_showing_up_"></span><span id="why_aren_t_my_subds_showing_up_"></span><span id="WHY_AREN_T_MY_SUBDS_SHOWING_UP_"></span>**Por que minha SUBDs não está aparecendo?**
</dt> <dd>

Não há suporte para SUBDs. Você pode convertê-los em malhas de polígono.

</dd> <dt>

<span id="Why_does_my_animation_in_the_X_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="why_does_my_animation_in_the_x_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="WHY_DOES_MY_ANIMATION_IN_THE_X_FILE_LOOK_DIFFERENT_THAN_THE_ANIMATION_IN_THE_PREVIEW_WINDOW__"></span>**Por que minha animação no arquivo X parece ser diferente da animação na janela de visualização?** 
</dt> <dd>

A janela de visualização não está animando na noção mais estrita da questão. Ele não está reproduzindo animação, mas sim sincronizando com o estado mais atual da cena do Maya. Quando a animação é exportada, as matrizes em cada transformação são decompostas em escala, rotação (Quaternion) e componentes de tradução (geralmente chamados de SRTs). SRTs são mais desejáveis do que as matrizes porque interpolarem bem, fornecem uma forma mais compacta dos dados e podem ser compactados de forma independente. Nem todas as matrizes podem dividir em SRTs. Se não puderem decompor, o SRTs resultante será desconhecido e, portanto, erros pequenos na animação poderão ser detectados. Os dois recursos do Maya que geralmente causam problemas durante a decomposição são distorceções e rotações fora do centro. Se você estiver encontrando esse problema, porque está usando escalas ou rotações fora do centro, considere adicionar transformações adicionais aumentando seu nível de hierarquia.

Quando a animação D3DX dá suporte a SRTs, ela tem esta aparência:

``` syntax
[S]x[R]x[T]
```

As matrizes de Maya são muito mais complicadas e exigem uma quantidade significativa de processo adicional, que tem esta aparência:

``` syntax
[SpInv]x[S]x[Sh]x[Sp]x[St]x[RpInv]x[Ro]x[R]x[Rp]x[Rt]x[T]
```

</dd> <dt>

<span id="I_skinned_my_mesh_with_RigidSkin_but_the_mesh__or_portion__isn_t_moving._Why__"></span><span id="i_skinned_my_mesh_with_rigidskin_but_the_mesh__or_portion__isn_t_moving._why__"></span><span id="I_SKINNED_MY_MESH_WITH_RIGIDSKIN_BUT_THE_MESH__OR_PORTION__ISN_T_MOVING._WHY__"></span>**Eu revestimento minha malha com RigidSkin, mas a malha (ou parte) não está se movendo. Por?** 
</dt> <dd>

Não há suporte para a aparência rígida de Maya no momento. Use uma aparência suave.

</dd> <dt>

<span id="Where_has_all_of_my_IK_gone_in_the_X-file__"></span><span id="where_has_all_of_my_ik_gone_in_the_x-file__"></span><span id="WHERE_HAS_ALL_OF_MY_IK_GONE_IN_THE_X-FILE__"></span>**Onde todas as minhas IK ficaram no arquivo X?** 
</dt> <dd>

Os arquivos X não dão suporte a IK. Em vez disso, as soluções IK são inclusas nos quadros armazenados no arquivo X.

</dd> <dt>

<span id="Why_do_none_of_my_materials_colors_show_up_except_DirectXShaders__"></span><span id="why_do_none_of_my_materials_colors_show_up_except_directxshaders__"></span><span id="WHY_DO_NONE_OF_MY_MATERIALS_COLORS_SHOW_UP_EXCEPT_DIRECTXSHADERS__"></span>**Por que nenhuma das cores dos materiais é exibida, exceto DirectXShaders?** 
</dt> <dd>

Atualmente, as extensões do DirectX para Maya dão suporte apenas ao material do DirectXShader para visualização e exportação. Em uma versão futura, outros materiais podem ter suporte.

</dd> </dl>

## <a name="xinput-questions"></a>Perguntas XInputs

<dl> <dt>

<span id="Can_I_use_DirectInput_to_read_the_triggers__"></span><span id="can_i_use_directinput_to_read_the_triggers__"></span><span id="CAN_I_USE_DIRECTINPUT_TO_READ_THE_TRIGGERS__"></span>**Posso usar o DirectInput para ler os gatilhos?** 
</dt> <dd>

Sim, mas atuam como o mesmo eixo. Portanto, você não pode ler os gatilhos independentemente com o DirectInput. Usando XInput, os gatilhos retornam valores separados.

Para obter mais informações sobre por que o DirectInput interpreta os gatilhos como um eixo, consulte [usando o controlador Xbox 360 com o DirectInput](/windows/desktop/xinput/xinput-and-directinput).

</dd> <dt>

<span id="How_many_controllers_does_XInput_support__"></span><span id="how_many_controllers_does_xinput_support__"></span><span id="HOW_MANY_CONTROLLERS_DOES_XINPUT_SUPPORT__"></span>**A quantos controladores o XInput dá suporte?** 
</dt> <dd>

O XInput dá suporte a 4 controladores conectados por vez.

</dd> <dt>

<span id="Does_XInput_support_non-common_controllers__"></span><span id="does_xinput_support_non-common_controllers__"></span><span id="DOES_XINPUT_SUPPORT_NON-COMMON_CONTROLLERS__"></span>**O XInput dá suporte a controladores não comuns?** 
</dt> <dd>

Não, não.

</dd> <dt>

<span id="Are_common_controllers_available_through_DirectInput__"></span><span id="are_common_controllers_available_through_directinput__"></span><span id="ARE_COMMON_CONTROLLERS_AVAILABLE_THROUGH_DIRECTINPUT__"></span>**Os controladores comuns estão disponíveis por meio do DirectInput?** 
</dt> <dd>

Sim, você pode acessar controladores comuns por meio do DirectInput.

</dd> <dt>

<span id="How_do_I_get_force_feedback_on_the_common_controllers__"></span><span id="how_do_i_get_force_feedback_on_the_common_controllers__"></span><span id="HOW_DO_I_GET_FORCE_FEEDBACK_ON_THE_COMMON_CONTROLLERS__"></span>**Como fazer obter feedback forçado sobre os controladores comuns?** 
</dt> <dd>

Use a função [**XInputSetState**](/windows/desktop/api/xinput/nf-xinput-xinputsetstate) .

</dd> <dt>

<span id="Why_does_my_default_audio_device_change__"></span><span id="why_does_my_default_audio_device_change__"></span><span id="WHY_DOES_MY_DEFAULT_AUDIO_DEVICE_CHANGE__"></span>**Por que meu dispositivo de áudio padrão muda?** 
</dt> <dd>

Ao conectar o headset, o headset do controlador atua como um dispositivo de áudio USB padrão, portanto, quando ele está conectado, o Windows muda automaticamente para usar esse dispositivo de áudio USB como padrão. Como o usuário provavelmente não quer que todo o áudio passe pelo Headset, ele precisará ajustá-lo manualmente de volta à configuração original.

</dd> <dt>

<span id="How_do_I_control_the_lights_on_the_controller__"></span><span id="how_do_i_control_the_lights_on_the_controller__"></span><span id="HOW_DO_I_CONTROL_THE_LIGHTS_ON_THE_CONTROLLER__"></span>**Como fazer controlar as luzes no controlador?** 
</dt> <dd>

As luzes no controlador são predeterminadas pelo sistema operacional e não podem ser alteradas.

</dd> <dt>

<span id="How_do_I_access_the_Xbox_360_button_in_my_applications__"></span><span id="how_do_i_access_the_xbox_360_button_in_my_applications__"></span><span id="HOW_DO_I_ACCESS_THE_XBOX_360_BUTTON_IN_MY_APPLICATIONS__"></span>**Como fazer acessar o botão do Xbox 360 em meus aplicativos?** 
</dt> <dd>

Desculpe, esse botão está reservado para uso futuro.

</dd> <dt>

<span id="Where_do_I_get_drivers__"></span><span id="where_do_i_get_drivers__"></span><span id="WHERE_DO_I_GET_DRIVERS__"></span>**Onde obtenho drivers?** 
</dt> <dd>

Os drivers estarão disponíveis por meio de Windows Update.

</dd> <dt>

<span id="How_is_controller_ID_determined__"></span><span id="how_is_controller_id_determined__"></span><span id="HOW_IS_CONTROLLER_ID_DETERMINED__"></span>**Como a ID do controlador é determinada?** 
</dt> <dd>

Na inicialização do XInput, a ID é determinada de forma não determinística pelo mecanismo de XInput e pelos controladores que estão conectados. Se os controladores estiverem conectados enquanto um aplicativo XInput estiver em execução, o sistema atribuirá ao novo controlador o menor número disponível. Se um controlador estiver desconectado, seu número será disponibilizado novamente.

</dd> <dt>

<span id="How_do_I_get_the_audio_devices_for_the_controller__"></span><span id="how_do_i_get_the_audio_devices_for_the_controller__"></span><span id="HOW_DO_I_GET_THE_AUDIO_DEVICES_FOR_THE_CONTROLLER__"></span>**Como fazer obter os dispositivos de áudio para o controlador?** 
</dt> <dd>

Use a função [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/xinput/nf-xinput-xinputgetdsoundaudiodeviceguids) . Consulte o exemplo de AudioController para obter detalhes.

</dd> <dt>

<span id="What_should_I_do_when_a_controller_is_unplugged__"></span><span id="what_should_i_do_when_a_controller_is_unplugged__"></span><span id="WHAT_SHOULD_I_DO_WHEN_A_CONTROLLER_IS_UNPLUGGED__"></span>**O que devo fazer quando um controlador está desconectado?** 
</dt> <dd>

Se o controlador estava em uso por um jogador, você deve pausar o jogo até que o controlador seja reconectado e o Player Pressione um botão para sinalizar que está pronto para não pausar.

</dd> </dl>

 

 