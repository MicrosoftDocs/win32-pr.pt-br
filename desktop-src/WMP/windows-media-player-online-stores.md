---
title: Lojas online do Windows Media Player
description: Lojas online do Windows Media Player
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Armazenamentos online do Windows Media Player, sobre
- lojas online, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640292"
---
# <a name="windows-media-player-online-stores"></a>Lojas online do Windows Media Player

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O Windows Media Player fornece funcionalidade que permite que os provedores de conteúdo de mídia digital integrem seus serviços ao Windows Media Player. A integração entre o Player e uma loja de mídia digital online fornece uma experiência agradável e abrangente para o usuário, incluindo a capacidade de localizar conteúdo, baixar e gerenciar arquivos, reproduzir conteúdo e copiar conteúdo para CDs ou dispositivos.

## <a name="contacting-microsoft"></a>Entrando em contato com a Microsoft

Se você deseja que seu repositório de mídia digital online seja integrado ao Windows Media Player, mas ainda não fez contato com a Microsoft, você pode começar enviando um email para a equipe virtual dos serviços do Windows Media Player. O endereço de email da equipe é mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Para obter mais informações

Para obter orientações técnicas sobre como usar uma variedade de SDKs do Windows Media para criar um serviço que oferece conteúdo de mídia digital licenciado, vá para o [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) e procure "criando uma assinatura online do Windows Media Player 10".

## <a name="online-stores-in-windows-media-player-9-series"></a>Lojas online no Windows Media Player 9 Series

O Windows Media Player 9 Series apresentou o conceito de lojas online. No Windows Media Player 9 Series, os provedores de loja online podem integrar seus serviços ao recurso de **Serviços Premium** do Windows Media Player.

## <a name="online-stores-in-windows-media-player-10"></a>Lojas online no Windows Media Player 10

No Windows Media Player 10, os serviços Premium foram renomeados como lojas online e os novos recursos a seguir foram adicionados:

-   O Windows Media Player fornece até três painéis de tarefas para serem usados pela loja online.
-   Quando um usuário escolhe, na interface do usuário do Player, para exibir mais informações sobre o conteúdo de mídia digital, o Windows Media Player chama a loja online para fornecer as informações.
-   Quando o usuário escolhe, na interface do usuário do Player, para comprar um item de mídia, a chamada do Windows Media Player na loja online para lidar com a compra.
-   A loja online pode fornecer um plug-in que o Windows Media Player chama para obter assistência com o gerenciamento de direitos digitais e o tempo de processamento em segundo plano.
-   As lojas online podem ser integradas com a instalação do Windows Media Player.

## <a name="online-stores-in-windows-media-player-11"></a>Lojas online no Windows Media Player 11

O Windows Media Player 11 apresenta um novo tipo de loja de música online, um que está mais profundamente integrado à interface do usuário do jogador. No Windows Media Player 11, os novos recursos a seguir foram adicionados para dar suporte a esse novo tipo de loja online.

-   O Windows Media Player baixa o catálogo de mídia do repositório online, para que o usuário possa navegar rapidamente pelo conteúdo da loja online.
-   O Windows Media Player exibe o conteúdo de música do repositório online no controle de exibição de árvore de biblioteca.
-   À medida que o usuário navega na interface do usuário do Player, o jogador chama a loja online para fornecer páginas da Web que aprimorem a experiência do usuário.
-   A loja online fornece um plug-in que manipula todos os aspectos da comunicação entre o Windows Media Player e a loja online. Por exemplo, o plug-in manipula o logon, a renovação de licenças, a atualização do catálogo, o download de conteúdo e a compra de conteúdo.
-   O Windows Media Player fornece comunicação avançada entre o Player e as páginas da Web que são fornecidas pela loja online e hospedadas no Player.

## <a name="types-of-online-stores"></a>Tipos de lojas online

Há dois tipos de lojas online: tipo 1 e tipo 2.

Um repositório tipo 1 fornece o nível mais avançado de integração com o Windows Media Player. Ele fornece um catálogo de música baixável e está profundamente integrado à interface do usuário do jogador. Os armazenamentos do tipo 1 são compatíveis com o Windows Media Player 11 e posterior.

Os repositórios do tipo 2, que têm suporte do Windows Media Player 9 Series e posterior, têm duas subcategorias: lojas de comércio e lojas de música.

Uma loja de comércio fornece a experiência mais básica fornecendo até três painéis de tarefas de serviço que exibem as páginas da Web do repositório.

Uma loja de música fornece uma experiência mais integrada para o usuário do que uma loja de comércio. Em uma loja de música, os usuários podem clicar em botões e links no Windows Media Player (fora das páginas da Web fornecidas pela loja) para executar ações como comprar um CD ou DVD, obter mais informações sobre um item de mídia específico ou exibir o painel de exibição do info Center. Em cada caso, o Windows Media Player chama o armazenamento de música atual para lidar com essas solicitações.

> [!Note]  
> Alguns documentos referem-se a lojas de comércio como serviços comerciais básicos e se referem a lojas de música como serviços de música integrados.

 

A tabela a seguir mostra os recursos disponíveis para os diferentes tipos de lojas online.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Recurso</th>
<th>Tipo 2 loja de comércio</th>
<th>Tipo 2 loja de música</th>
<th>Armazenamento do tipo 1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Criar painéis de tarefas de serviço
<blockquote>
[!Note]<br />
O Windows Media Player 10 tem até três painéis de tarefas de serviço. O Windows Media Player 11 tem apenas um.
</blockquote>
<br/></td>
<td>Sim</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="even">
<td>Altere a aparência do armazenamento alterando atributos como cor do botão, cor da barra de tarefas e texto do botão.</td>
<td>Sim</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="odd">
<td>Adicione imagens de logotipo ao menu e à barra de tarefas da loja online do Windows Media Player.</td>
<td>Sim</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="even">
<td>Navegue de HTMLView para a loja online.</td>
<td>Sim</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="odd">
<td>Manipule as solicitações do Windows Media Player para comprar um CD ou DVD.</td>
<td>Não</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="even">
<td>Manipule as solicitações do Windows Media Player para fornecer informações avançadas sobre o álbum.</td>
<td>Não</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="odd">
<td>Forneça a página da Web de exibição do info Center.</td>
<td>Não</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="even">
<td>Personalize a instalação do Windows Media Player para especificar uma loja online inicial.</td>
<td>Não</td>
<td>Sim</td>
<td>Sim</td>
</tr>
<tr class="odd">
<td>Forneça um plug-in que implemente <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.
<blockquote>
[!Note]<br />
No Windows Media Player 10 e posterior, esse plug-in também pode implementar <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.
</blockquote>
<br/></td>
<td>Não</td>
<td>Sim</td>
<td>Não</td>
</tr>
<tr class="even">
<td>Fornecer um catálogo de música que é baixado pelo Windows Media Player</td>
<td>Não</td>
<td>Não</td>
<td>Sim</td>
</tr>
<tr class="odd">
<td>Forneça páginas da Web personalizadas e menus de contexto com base na navegação do usuário durante a interface do usuário do jogador.</td>
<td>Não</td>
<td>Não</td>
<td>Sim</td>
</tr>
<tr class="even">
<td>Forneça um plug-in que implemente <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>.</td>
<td>Não</td>
<td>Não</td>
<td>Sim</td>
</tr>
</tbody>
</table>



 

O restante da documentação sobre lojas online é dividido nas seções a seguir.



| Seção                                                                                                                              | Descrição                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit de boas-vindas de lojas online](online-stores-welcome-kit.md)                                                                           | Contém informações sobre como colocar uma loja de mídia digital online integrada no Windows Media Player.             |
| [Tipos 1 lojas online](type-1-online-stores.md)                                                                                     | Contém seções sobre, guia e referência para lojas online do tipo 1.                                             |
| [Tipo 2 lojas online](type-2-online-stores.md)                                                                                     | Contém seções sobre, guia e referência para lojas online do tipo 2.                                             |
| [Informações comuns às lojas online tipo 1 e tipo 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contém informações que se aplicam às lojas online tipo 1 e tipo 2.                                          |
| [Atualizando licenças para lojas que têm o logotipo do PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Contém informações sobre como lojas online que não estão integradas ao Windows Media Player podem atualizar licenças. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**SDK do Windows Media Player**](windows-media-player-sdk.md)
</dt> </dl>

 

 





