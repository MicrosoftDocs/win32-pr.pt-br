---
title: Como obter uma loja de música online no quadro
description: Como obter uma loja de música online no quadro
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player Lojas Online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e618f1eddca3389801d2b6c2d5de1e7a6ee67f7aef593478f4999f69bbd148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390876"
---
# <a name="getting-an-online-music-store-on-board"></a>Como obter uma loja de música online no quadro

Este tópico descreve o processo de colocar um armazenamento de mídia digital online no quadro para Windows Media Player. O tempo necessário para o processo de entrada do início ao fim é de aproximadamente 45 a 60 DIAS ÚTEIS. Os dois estágios do processo de entrada são descritos na tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Estágio</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pendente</td>
<td><ul>
<li>Você envia à Microsoft as informações de contato necessárias, as informações de inicialização e as contas de validação.</li>
<li>A Microsoft envia uma chave de teste e uma chave de produção.</li>
<li>Você testa sua loja online com Windows Media Player.</li>
<li>Você envia contratos e contratos assinados para a Microsoft.</li>
</ul></td>
</tr>
<tr class="even">
<td>Validação</td>
<td>A Microsoft valida sua loja online.</td>
</tr>
</tbody>
</table>



 

Depois de concluir os estágios pendentes e de validação, a Microsoft publicará sua loja online.

## <a name="pending-stage"></a>Estágio pendente

O estágio pendente oferece a oportunidade de testar sua loja online Windows Media Player. Também é um bom momento para garantir que todos os contratos e contratos necessários sejam assinados. Para começar, envie à Microsoft as seguintes informações, conforme definido posteriormente neste tópico:

-   Informações de contato
-   Informações de inicialização
-   Contas de validação

Após o recebimento de suas informações de contato e inicialização, a Microsoft enviará uma chave de teste e uma chave de produção. Depois de adicionar sua chave de teste ao Registro e reiniciar o Player, sua loja online aparecerá no Player e você poderá testá-la. Para obter informações sobre onde colocar sua chave de teste no Registro, consulte Chaves e entradas do Registro para um Tipo [1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md) ou Chaves e Entradas do Registro para um Tipo [2 Online Store.](registry-keys-and-entries-for-a-type-2-online-store.md)

Você deve testar todos os aspectos da sua loja online, incluindo sua interface do usuário e seu plug-in. Como parte do processo de teste, você deve executar os testes descritos em Testes de validação para lojas de música [online do tipo 2.](validation-tests-for-type-2-online-music-stores.md)

> [!Note]  
> Os armazenamentos do tipo 1 devem passar em todos os testes de validação para lojas do tipo 2, além de alguns testes adicionais específicos para a experiência de tipo 1. Para obter informações sobre testes de validação do tipo 1, entre em contato com a equipe virtual Windows Media Player Services em mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Informações de contato

A tabela a seguir mostra as informações de contato que a Microsoft requer para sua loja online. Preencha o [formulário Informações de Contato](contact-information-form-for-an-online-music-store.md) e envie-o para a equipe virtual Windows Media Player Services em mpsvctm@microsoft.com .



| Item                     | Descrição                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nome da Loja               | O nome da marca da sua loja                                                            |
| Nome do Provedor            | O nome da empresa de rótulo branco/provedor (se diferente)                               |
| Localidade da Loja             | As Windows locais de usuário em que seu armazenamento deve ser exibido                                |
| Categoria da Loja           | Música, Rádio, Filme, TV, Esportes, Notícias, Audio- Entretenimento e/ou Outros (descreva) |
| Modelo de Compra           | Comprar, Aluguel, Assinatura e/ou Outros (descreva)                            |
| Idioma da Loja           |                                                                                           |
| Nome(s) de contato do armazenamento    |                                                                                           |
| Email(s) de contato do armazenamento  |                                                                                           |
| Conta(s) do MSFT Passport | Isso é para possíveis indicações futuras em programas beta e de desenvolvimento de parceiros.         |
| Endereço de envio         | Sem P.O. Caixas                                                                             |
| City                     |                                                                                           |
| Estado                    |                                                                                           |
| Código postal              |                                                                                           |
| País/Região           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contato da pesquisa           | Tudo bem se entrarmos em contato com você sobre sua experiência com o programa no futuro?        |



 

## <a name="startup-information"></a>Informações de inicialização

Para cada região geográfica que sua loja atenderá, envie à Microsoft um conjunto de informações de inicialização para seu armazenamento de teste, um conjunto de informações de inicialização para seu armazenamento de produção e um conjunto de contas de validação.

O tópico [Formulário de Informações de Inicialização](startup-information-form-for-an-online-music-store.md) para uma Loja de Música Online contém duas cópias do formulário Informações de Inicialização e uma cópia do formulário Contas de Validação. Preencha os formulários e envie-os para a equipe virtual Windows Media Player Services em mpsvctm@microsoft.com .

A tabela a seguir descreve as informações de inicialização que a Microsoft requer para sua loja online.



| Item                                                                                                     | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL XML de informações de serviço (limite de 2048 caracteres)                                                              | A URL em que Windows Media Player obtém o [documento XML ServiceInfo](serviceinfo-document.md).                                                                                                                                         |
| Chave de serviço (ID exclusiva)                                                                                  | Uma cadeia de caracteres que identifica exclusivamente sua loja online. Você deve criar um para produção e outro para teste (por exemplo, "MyStore" e "MyStoreTest"). Observe que uma chave de serviço não é a mesma coisa que uma chave de teste.                        |
| Nome amigável (limite de 30 caracteres)                                                                       | O nome da loja que é exibido no seletor Windows Media Player serviço.                                                                                                                                                        |
| URL da imagem de menu (limite de 2048 caracteres)                                                                    | A URL em Windows Media Player recupera o logotipo de 15 x 15 pixels que ele exibe no seletor de serviço.                                                                                                                                 |
| Comprar URL de Música (limite de 2048 caracteres)<br/> (Somente lojas de música integradas)<br/>                | A URL usada pelos links "Comprar CD" e "Comprar música online" do player.                                                                                                                                                              |
| URL de compra de interface do usuário de 10 pés (limite de 2048 caracteres)<br/> (Somente lojas de música integradas – opcional)<br/> | A URL usada pelos links "Comprar CD" e "Comprar música online" do Player no Windows XP Media Center Edition e no Windows Media Center no Windows Vista.                                                                              |
| Logotipo da Loja (130w x 30h)<br/> (Anexar o arquivo PNG separadamente.)<br/>                              | O logotipo da loja que é exibido na dica de ferramenta que aparece quando o mouse está sobre a imagem browse-all. Esse logotipo deve ser um arquivo formatado em PNG e, preferencialmente, com combinação alfa, para que possa se ajustar às alterações de cor no Windows Media Player. |
| Imagem Browse-all (108w x 108h)<br/> (Anexar o arquivo PNG separadamente.)<br/>                       | A breve descrição na dica de ferramenta que aparece quando o mouse está sobre sua imagem browse-all.                                                                                                                                               |
| Armazenar texto de descrição (limite de 110 caracteres)                                                             | O texto que aparece na dica de ferramenta abaixo do texto de descrição do armazenamento.                                                                                                                                                                        |
| Texto para hiperlink (limite de 45 caracteres)                                                                  | O logotipo da loja exibido na página Procurar todas as Lojas Online. Ele deve ser um arquivo formatado em PNG e, preferencialmente, com combinação alfa para que possa se ajustar às alterações de cor no Windows Media Player.                                           |



 

> [!Note]  
> A imagem browse-all de 108 x 108 pixels é um requisito para Windows Media Player 11 e posteriores.

 

> [!Note]  
> No Windows Media Player 11 e posterior, os elementos ServiceTask2 e ServiceTask3 do documento XML ServiceInfo são ignorados. Para obter informações detalhadas sobre o documento XML ServiceInfo, consulte [Documento ServiceInfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Contas de validação

Para concluir o processo de validação descrito na seção Estágio de Validação a seguir, a Microsoft requer cinco (5) contas de validação para cada tipo de conta que sua loja online oferece. Por exemplo, se você oferecer contas que diferenciam entre recursos e funcionalidades, como básica e premium, a Microsoft precisará de cinco (5) contas de validação para cada tipo, para um total de dez (10) contas.

Envie o nome de usuário e a senha de cada conta de validação para mpsvctm@microsoft.com . Inclua também o nome de uma pessoa que a Microsoft pode contatar em relação às contas de validação. Essas contas serão usadas para validação mensal contínua, portanto, inclua um processo para "recarregar" as contas. Um dos problemas mais comuns ocorre quando uma loja online não fornece crédito de compra suficiente para a Microsoft validar todos os cenários de compra. As contas devem permanecer ativas depois que o processo de entrada for concluído.

## <a name="validation-stage"></a>Estágio de validação

Durante o estágio de validação, a Microsoft verifica se os principais recursos de sua loja online funcionam corretamente. Para todas as lojas (tipo 1 e tipo 2), a Microsoft executa os testes de verificação detalhados em Testes de validação para lojas de música online do tipo [2.](validation-tests-for-type-2-online-music-stores.md) A Microsoft também executa alguns testes de validação adicionais para lojas do tipo 1. Se você tiver dúvidas sobre o estágio de validação para lojas do tipo 1, envie um email para mpsvctm@microsoft.com .

Durante o estágio de validação, a Microsoft faz duas aprovações de validação. A primeira passagem se aplica ao Release Candidate 1 (RC1) de sua loja online. Se o seu armazenamento passar na validação rc1, você deverá bloqueá-lo e não fazer mais alterações. A Microsoft fará uma segunda passagem de validação em sua loja mesmo que sua loja passe na validação rc1.

Se o armazenamento falhar em qualquer parte da aprovação de validação do RC1, você terá duas semanas para criar uma segunda versão release candidate (RC2), que a Microsoft validará durante a aprovação de validação do RC2.

Se o armazenamento falhar em qualquer parte da validação do RC2, você deverá aguardar até o lançamento a seguir.

## <a name="test-and-production-keys"></a>Chaves de teste e produção

Lembre-se de que, durante o estágio pendente, você enviou à Microsoft dois conjuntos de informações de inicialização: um para seu armazenamento de teste e outro para o armazenamento de produção. Lembre-se também de que a Microsoft enviou duas chaves: uma chave de teste e uma chave de produção.

A chave de teste é totalmente para seu próprio uso. Quando sua chave de teste estiver no Registro, Windows Media Player a URL serviceInfo enviada para o seu armazenamento de teste.

Quando sua chave de produção estiver no Registro, Windows Media Player a URL serviceInfo enviada para o armazenamento de produção. A Microsoft usa sua chave de produção durante o estágio de validação. A Microsoft nunca usa sua chave de teste para validação.

Quando sua loja estiver em tempo real, Windows Media Player a URL serviceInfo enviada para seu armazenamento de produção.

Como regra geral, seu armazenamento de teste deve ser o local em que você desenvolve seu serviço e faz alterações diárias. Seu armazenamento de produção deve ser o local em que você mantém uma versão estável do serviço.

## <a name="common-on-boarding-problems"></a>Problemas comuns de entrada

Aqui estão alguns problemas comuns que podem fazer com que seu armazenamento falhe no teste de validação.

-   Falha ao fazer a transição de servidores de teste para servidores de produção. Isso leva a muitos problemas, como páginas ausentes, configurações de segurança e IIS inválidas e contas de teste que não funcionam mais.
-   O link Comprar (ou o link Comprar) na área Agora Em reprodução é inválido. Isso pode fazer com que sua loja falhe na validação mesmo quando todo o resto estiver funcionando.
-   A equipe de validação da Microsoft testará vários cenários de compra, desde pequenas compras até compras muito grandes. Você deve fornecer uma maneira acessível para que eles atuem como um consumidor em sua loja. Sua loja não poderá ser validada se a equipe de validação não tiver créditos de compra suficientes para validar todos esses cenários.

Para obter uma lista mais completa de problemas comuns de entrada e perguntas frequentes compiladas pela Equipe Virtual do Windows Media Player Services, consulte Problemas comuns de entrada para lojas de música [online.](common-on-boarding-problems-for-online-music-stores.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Kit de boas-vindas de lojas online](online-stores-welcome-kit.md)
</dt> </dl>

 

 





