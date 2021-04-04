---
title: Práticas recomendadas de instalação para jogos online com vários participantes
description: Este artigo descreve a criação de uma cadeia de design de confiança para instalação de cliente de jogos online de vários participantes (MMOG) e sistemas de atualização de jogos personalizados que funcionam bem com o Windows e o modelo de segurança do Windows Vista e do Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81003a434b830f046c29d606355104fe618d1f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007782"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Práticas recomendadas de instalação para jogos online com vários participantes

Este artigo descreve a criação de uma cadeia de design de confiança para instalação de cliente de jogos online de vários participantes (MMOG) e sistemas de atualização de jogos personalizados que funcionam bem com o Windows e o modelo de segurança do Windows Vista e do Windows 7. A abordagem foi projetada para habilitar a aplicação de patches em títulos de MMOG enquanto dá suporte a contas de usuário padrão, que têm acesso restrito ao registro do sistema e do disco rígido.

-   [Por que os clientes do MMOG têm requisitos diferentes para jogos tradicionais de varejo adquiridos](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Visão geral de uma abordagem de cadeia de confiança](#overview-of-a-chain-of-trust-approach)
-   [Tudo é validado no servidor, por que devo me preocupar se meu cliente é invadido?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Construção do aplicativo de carregador de Trust-Worthy](#construction-of-the-trust-worthy-loader-application)
    -   [Leitura em segundo plano](#background-reading)
    -   [Instalação do carregador confiável e Patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Instalação dos executáveis, DLLs e dados do jogo](#installation-of-the-game-executables-dlls-and-data)
    -   [Código de modificação da lista de controle de acesso](#access-control-list-modification-code)
    -   [Instalações para usuários avançados](#installations-for-advanced-users)
    -   [A verificação de confiança do carregador](#the-loaders-verification-of-trust)
    -   [Validação de dados](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Por que os clientes do MMOG têm requisitos diferentes para jogos tradicionais de varejo adquiridos

A natureza constantemente conectada e em constante evolução do MMOGs torna um requisito fundamental para fornecer atualizações regulares do código do cliente e do conteúdo para corrigir vulnerabilidades de segurança e estender a experiência de jogos. Com o potencial para atualizações quase diárias, o cenário de MMOG requer um gerenciamento cuidadoso para garantir uma experiência amigável do usuário. Isso difere do modelo de compra de varejo tradicional, em que um pequeno número de patches pode ser fornecido próximo à data de envio de varejo do produto. A Windows Installer tecnologia limitada de aplicação de patches do usuário fornecida com o sistema operacional foi projetada para lidar com pequenas quantidades de patches de aplicativos, e não a grande quantidade e alta frequência necessária para MMOGs. Portanto, geralmente é necessário que os sistemas de aplicação de patches personalizados sejam desenvolvidos para atender às necessidades do MMOGs, incluindo quaisquer requisitos especiais específicos para o MMOG específico que está sendo desenvolvido.

Como muitos computadores estão conectados à Internet, o Windows Vista e o Windows 7 têm restrições de segurança e proteções mais difíceis para os usuários, que limitam o acesso que os aplicativos têm a várias áreas do disco rígido. Ao contrário do Windows XP, essas restrições são habilitadas para o modo padrão para contas de usuário. Essas restrições devem ser levadas em conta ao criar o layout de um jogo, de um executável e de dados e de seu sistema de aplicação de patches associado. Para obter mais detalhes sobre as medidas de segurança fornecidas pelo sistema operacional, consulte [controle de conta de usuário para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Visão geral de uma abordagem de cadeia de confiança

A abordagem de atualização personalizada apresentada neste white paper baseia-se em ter um aplicativo de carregador confiável instalado na pasta arquivos de programas protegidos, mantendo os arquivos executáveis e os dados de jogos em uma área compartilhada de todos os usuários. Uma cadeia de confiança começa com o carregador que executa verificações de validade nos dados e binários do jogo antes do lançamento.

![a cadeia de confiança começa com um carregador confiável](images/mmo-installation-best-practices-01.gif)

O carregador confiável precisa ter lógica suficiente para poder verificar se o executável do jogo e outros binários não foram adulterados antes de iniciar o jogo. O carregador também pode verificar os dados do jogo sempre que necessário. no entanto, o tamanho dos dados do jogo geralmente é muito grande para permitir que ele seja verificado todas as vezes em uma única passagem. Uma abordagem alternativa é usar um padrão de amostragem que garanta que a verificação de todo o conjunto de dados ocorra durante um longo período de tempo. O aplicativo de carregador pode conter um mecanismo de aplicação de patches de jogos, que fornece um método digno de confiança pelo para integrar atualizações com o jogo instalado.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Tudo é validado no servidor, por que devo me preocupar se meu cliente é invadido?

É impossível confiar que o cliente não foi comprometido; Portanto, é comum que servidores MMOG validem todos os dados recebidos do cliente. Embora esse processamento possa identificar clientes de jogos comprometidos ou trapaceandodos no universo do jogo, o servidor não pode identificar facilmente todos os problemas aos quais o cliente do jogo pode ser exposto. É importante reforçar a proteção contra hackers que desejam usar seu cliente como uma plataforma para ataques em seu serviço, outros usuários ou até mesmo como um vetor para atacar os próprios computadores cliente. A aplicação de assinaturas de código e técnicas de verificação de dados pode ajudar a detectar clientes comprometidos antes que eles sejam executados. Como o mecanismo de aplicação de patches requer a exposição de binários executáveis e DLL que não são protegidos pelas permissões somente leitura padrão em arquivos de programas, a validação desses arquivos antes de iniciá-los é importante para a segurança geral do sistema.

Esse modelo não tenta lidar com o cenário do usuário administrador mal-intencionado em que o próprio carregador pode se tornar comprometido, mas se concentra em proteger usuários padrão contra acidentalmente execução de código adulterado. As técnicas tradicionais de validação de servidor-cliente são, na verdade, a única mitigação possível para administradores de sistema cliente mal-intencionados.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Construção do aplicativo de carregador de Trust-Worthy

### <a name="background-reading"></a>Leitura em segundo plano

Os leitores devem se familiarizar com a documentação a seguir, que fornece detalhes da tecnologia base para garantir a prática recomendada para a confiança baseada em software.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Assinatura de código
</dt> <dd>

[Assinatura Authenticode para desenvolvedores de jogos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) no MSDN

</dd> </dl>

A seção a seguir detalha as APIs que devem ser usadas para construir o aplicativo de carregador, que dá suporte ao layout de disco para instalação e verificação de verificação de confiança.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Instalação do carregador confiável e Patcher

O carregador confiável e a versão base do utilitário Patcher devem ser instalados na pasta arquivos de programas protegidos no HDD, assim como nas instalações tradicionais. A instalação e a aplicação de patches do aplicativo carregador exigem direitos de administrador, portanto, é importante minimizar a frequência de atualização para o carregador para garantir que os usuários finais não precisem aumentar com frequência, embora Windows Installer aplicação limitada de patches de usuário possa ser usada para evitar a elevação de patches do carregador.

Consulte o artigo corrigindo o software de jogos no Windows XP, no Windows Vista e no Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Instalação dos executáveis, DLLs e dados do jogo

Para facilitar as atualizações de usuário padrão do jogo sem privilégios administrativos, o executável dos jogos, as DLLs e os dados devem ser instalados em uma área do disco rígido que está acessível para gravação para todos os usuários. O sistema operacional fornece uma área de "todos os usuários de aplicativos" que pode ser usada como o local padrão para instalação. [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) deve ser usado com a chave de \_ AppData comuns de CSIDL \_ para determinar o caminho do arquivo para essa área. É importante que não sejam feitas suposições sobre o caminho para o qual essa chave retorna, como pode ser configurável pelo usuário.

A instalação precisa alterar ou gerenciar as permissões de pasta para obter o acesso de todos os usuários-compartilhado-gravação necessário para atualizar o título. Com as permissões corretas, a funcionalidade de atualizador do jogo do programa carregador pode facilmente corrigir o jogo sem a necessidade de um privilégio especial de qualquer conta de usuário, incluindo vezes quando iniciado por usuários padrão.

### <a name="access-control-list-modification-code"></a>Código de modificação da lista de controle de acesso

Para o Windows XP, você precisará executar o código para alterar a lista de controle de acesso (ACL) manualmente, aqui está uma função de exemplo que demonstra como fazer isso:

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

Este exemplo de código também funcionará para o Windows Vista e o Windows 7; no entanto, eles também fornecem o utilitário de linha de comando icacls para editar ACLS de arquivo que você pode optar por usar em vez disso.

A ferramenta fornece uma ajuda detalhada quando executada no entanto, um exemplo de uso para a ferramenta é:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Esse uso concederá ao usuário a permissão Excluir e gravar permissões DAC para a pasta de jogos armazenada nas áreas todos os usuários do disco rígido.

### <a name="installations-for-advanced-users"></a>Instalações para usuários avançados

Para cenários avançados de instalação de usuário, um usuário pode querer especificar o caminho de instalação de jogos manualmente. A seleção de diretório deve ser restrita a uma fora dos arquivos de programa para garantir que a pasta esteja em uma área verdadeiramente compartilhável do disco rígido. O caminho selecionado pelo usuário deve ser usado apenas para os EXEs e os dados dos jogos como o carregador de jogos e os EXEs do Patcher sempre devem ser instalados na pasta arquivos de programas seguros para obter mais segurança.

### <a name="the-loaders-verification-of-trust"></a>A verificação de confiança do carregador

O Windows fornece a função [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) para verificar a validade do código assinado e é baseado nos serviços de criptografia no sistema operacional. A função está totalmente documentada na função MSDN: **WinVerifyTrust** .

O programa de exemplo a seguir no MSDN detalha o uso da função para determinar se um executável de programa está assinado com um certificado válido: [programa C de exemplo: verificando a assinatura de um arquivo PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).

Para fins de verificação de que o executável do jogo assinado é confiável para ser executado de dentro do carregador, a ação de verificação genérica será suficiente:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

\_Verificação genérica de ação WINTRUST \_ \_ \_ v2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Significado
</dt> <dd>

Verifique um arquivo ou objeto usando o provedor de diretiva Authenticode.

</dd> </dl>

A função usa um argumento de estrutura de entrada que contém informações que o provedor de confiança precisa para processar a ação especificada. Normalmente, como no caso de exemplo anterior, a estrutura inclui informações que identificam o objeto que o provedor de confiança deve avaliar.

O formato da estrutura é específico para o identificador de ação. O tópico a seguir sobre o MSDN detalha a estrutura de exemplo para a estrutura de [**\_ dados**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) do provedor de wintrust: wintrust.

Se o provedor de confiança verificar que o assunto é confiável para a ação especificada, o valor de retorno será zero. Nenhum outro valor além de zero deve ser considerado um retorno bem-sucedido.

### <a name="data-validation"></a>Validação de dados

O mecanismo de codesignação só dá suporte à assinatura de alguns tipos específicos de arquivos, incluindo executáveis, DLLs, pacotes de Windows Installer (arquivos. msi) e arquivos de gabinete (. cab). A API [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) não deve ser usada para verificar se arquivos de dados grandes (arquivos. cab, por exemplo) não foram adulterados, pois há alguns problemas de desempenho e estabilidade ao validar arquivos muito grandes. Os executáveis do programa tendem a ser pequenos o suficiente para que uma verificação de confiança total ocorra usando o provedor WinTrust, mas os arquivos de dados para jogos são geralmente do realm de muitos gigabytes. A abordagem adotada pelo carregador para a verificação dos dados do jogo deve ser aquela em que uma pequena amostra do conjunto é testada no tempo de execução do jogo. Essa abordagem espalha o custo dos testes de verificação durante a vida útil da experiência do jogo e pode fornecer uma experiência de usuário tranqüila sem tempos de espera longos. Para conseguir isso, a organização cuidadosa dos dados pode ser necessária. Alguns MMOGs empregam uma abordagem de banco de dados para ajudar a gerenciar, manter e verificar a exatidão dos ativos do jogo ao longo do tempo.

Do ponto de vista da segurança, o código do cliente deve ser criado para não confiar em arquivos de dados, mesmo se você estiver usando algum tipo de validação de dados básica com o carregador confiável. Verificações de cabeçalho, hashes e outra verificação de integridade tradicional devem ser empregadas. O trabalho para proteger o código de e/s do cliente também deve ser feito usando técnicas como teste de fuzzing, bem como tirando proveito de ferramentas de análise de código estático automáticas, como a opção **/Analyze** no visual Studio 2005 e no visual Studio 2008 (disponível no Visual Studio Team System e o compilador gratuito fornecido com o SDK do Windows).

Para obter mais informações sobre segurança de software, consulte [práticas recomendadas de segurança no desenvolvimento de jogos](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 