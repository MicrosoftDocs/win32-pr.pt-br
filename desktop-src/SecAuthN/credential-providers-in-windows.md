---
description: Provedores de credenciais no Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Provedores de credenciais no Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38543127709007407c013a2a8ff047f7c91f4440351653061e894f4e7c2d90d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008794"
---
# <a name="credential-providers-in-windows-10"></a>Provedores de credenciais no Windows 10

Os provedores de credenciais são o mecanismo principal para autenticação de usuário — atualmente, eles são o único método para os usuários comprovarem sua identidade, que é necessária para o logon e outros cenários de autenticação do sistema. com Windows 10 e a introdução do Microsoft Passport, os provedores de credenciais são mais importantes do que nunca; Eles serão usados para autenticação em aplicativos, sites e muito mais.

a Microsoft fornece uma variedade de provedores de credenciais como parte do Windows, como senha, PIN, cartão inteligente e Windows Hello (reconhecimento de impressão digital, facial e íris). Eles são chamados de "provedores de credenciais do sistema" neste artigo. OEMs, empresas e outras entidades podem escrever seus próprios provedores de credenciais e integrá-los facilmente ao Windows. Eles são chamados de "provedores de credenciais de terceiros" neste artigo. Observe que os provedores de credenciais v1 e v2 têm suporte no Windows 10. É importante que os criadores e gerentes de provedores de credenciais de terceiros compreendam essas recomendações.

## <a name="system-credential-providers"></a>Provedores de credenciais do sistema

É altamente recomendável que sempre haja pelo menos um provedor de credencial do sistema disponível para cada usuário no dispositivo, além de qualquer provedor de credenciais de terceiros. Além disso, durante a configuração do provedor de credenciais de terceiros, cada usuário no dispositivo deve ser solicitado a configurar pelo menos um provedor de credenciais do sistema (se nenhuma outra opção de recuperação estiver disponível; consulte o cenário A, abaixo).

### <a name="scenario-a"></a>Cenário A

Um usuário de conta local configurou um provedor de credenciais de terceiros e usa-o regularmente para fazer logon no dispositivo. Um dia, o usuário instala algumas atualizações no dispositivo que interrompe o provedor de credenciais de terceiros e o usuário não está ciente dessa alteração antes de reiniciar o computador.

Na próxima reinicialização, o usuário estará na tela de logon e não poderá usar o provedor de credenciais de terceiros esperado. Se o usuário tiver configurado um provedor de credenciais do sistema, o usuário poderá fazer logon no computador usando-o. Caso contrário, o usuário não tem como recuperar a conta no computador.

### <a name="scenario-b"></a>Cenário B

Um usuário da conta MSA/AD/AAD configurou um provedor de credenciais terceirizado e usa-o regularmente para fazer logon no dispositivo. Um dia, o usuário instala algumas atualizações no dispositivo que interrompe o provedor de credenciais de terceiros e o usuário não está ciente dessa alteração antes de reiniciar o computador.

Na próxima reinicialização, o usuário estará na tela de logon e não poderá usar o provedor de credenciais de terceiros esperado. Se o usuário tiver configurado um provedor de credenciais do sistema, o usuário poderá fazer logon no computador usando-o. Como alternativa, se o provedor de credenciais de senha do sistema estiver disponível, o usuário poderá solicitar/redefinir a senha remotamente e usá-la para fazer logon no computador. Se nenhuma opção estiver disponível, o usuário não terá como recuperar a conta no computador.

### <a name="conclusion"></a>Conclusão

Em resumo, queremos desencorajar a desabilitação de todos os provedores de credenciais do sistema em um dispositivo. Embora os provedores de credenciais de terceiros possam atender aos requisitos de autenticação adicionais para determinados grupos de usuários, é muito importante garantir que o usuário sempre possa reobter o acesso à sua máquina quando ocorrer uma alteração significativa. Os provedores de credenciais do sistema fornecem essa garantia.

## <a name="custom-credential-providers"></a>Provedores de credenciais personalizados

o Windows framework do provedor de credenciais permite que os desenvolvedores criem provedores de credenciais personalizados. Quando o [Winlogon](winlogon.md) deseja coletar credenciais, a interface do usuário de logon consulta cada provedor de credenciais para obter o número de credenciais que deseja enumerar. Depois que todos os provedores tiverem enumerado seus blocos, a interface do usuário de logon os exibirá para o usuário. O usuário interage com um bloco para fornecer as credenciais necessárias. A interface do usuário de logon envia essas credenciais para autenticação. Os provedores de credenciais também podem ser usados pela interface do usuário da credencial quando as credenciais são necessárias. Consulte [**\_ cenário de \_ uso \_ do provedor de credenciais**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) para obter uma lista de cenários em que um provedor de credenciais pode ter suporte.

Graças a esse sistema, é muito mais fácil criar um provedor de credenciais do que era historicamente. Grande parte do trabalho é tratada pela combinação de [Winlogon](winlogon.md), a interface do usuário de logon e a interface do usuário da credencial. Para fazer isso, você precisará criar sua própria implementação de [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) e [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential). Se você estiver implementando um provedor de credenciais v2, que é recomendado, também precisará implementar o [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2).

É importante observar que os provedores de credenciais não são mecanismos de imposição. Eles são usados simplesmente para reunir e serializar credenciais, enviando-as para autorização. A autoridade local e os pacotes de autenticação serão tratados e qualquer imposição de segurança necessária.

combinando provedores de credenciais com hardware com suporte, você pode estender Windows para dar suporte ao logon com informações biométricas, senhas, PINs, certificados de cartão inteligente ou qualquer pacote de autenticação personalizado que você escolher criar. Você também pode personalizar a experiência de logon para o usuário de várias maneiras. Por exemplo, quando a interface do usuário de logon consulta seu provedor de credenciais para os blocos de credencial, você pode especificar um bloco padrão para fornecer uma experiência personalizada para um usuário. Os provedores de credenciais podem até mesmo ser projetados para dar suporte ao SSO (logon único), autenticar usuários em um ponto de acesso seguro, bem como logon no computador.

os provedores de credenciais são registrados em um computador Windows e são responsáveis pelo seguinte.

-   Descrever as informações de credenciais necessárias para a autenticação.
-   Tratamento da comunicação e da lógica com qualquer autoridade de autenticação externa.
-   Empacotando as credenciais para logon interativo e de rede.

> [!TIP]
>
> Tenha em mente que vários provedores de credenciais podem ser instalados em um único computador.

## <a name="wrapping-credential-providers"></a>Encapsulando provedores de credenciais

O encapsulamento de um provedor de credenciais do sistema pode ser feito para adicionar funcionalidade a esse provedor de credenciais que não tem suporte nativo. Isso não é recomendado porque pode levar a um comportamento problemático. As alterações podem ser feitas no provedor de credenciais que podem entrar em conflito com o wrapper, causando uma experiência de usuário ruim ou até mesmo impedindo o usuário de entrar em seu dispositivo. Isso é especialmente verdadeiro com a cadência de atualização frequente de Windows 10.

Se a funcionalidade em um provedor de credenciais for necessária e não estiver incluída nativamente, o caminho recomendado será criar um provedor de credenciais personalizado. Essa é uma abordagem mais estável que não assume dependências dos provedores do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[experiência de Logon Windows controlada pelo provedor de credenciais](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[\_serialização de \_ credencial do provedor de credenciais \_](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_cenário de \_ uso do provedor de credenciais \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
