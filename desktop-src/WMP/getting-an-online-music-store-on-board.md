---
title: Como obter uma loja de música online no painel
description: Como obter uma loja de música online no painel
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Lojas online do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c5d13e14e95e88e83d42fd7d5cd00551bb507
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916481"
---
# <a name="getting-an-online-music-store-on-board"></a>Como obter uma loja de música online no painel

Este tópico descreve o processo de colocar uma loja de mídia digital online no painel do Windows Media Player. O tempo necessário para o processo de integração do início ao fim é de aproximadamente 45-60 dias úteis. Os dois estágios do processo de integração são descritos na tabela a seguir.



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
<li>Você testa sua loja online com o Windows Media Player.</li>
<li>Você envia contratos assinados e contratos à Microsoft.</li>
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

O estágio pendente oferece a oportunidade de testar sua loja online no Windows Media Player. Também é um bom momento para garantir que todos os contratos e acordos necessários sejam assinados. Para começar, envie a Microsoft as seguintes informações, conforme definido mais adiante neste tópico:

-   Informações de contato
-   Informações de inicialização
-   Contas de validação

Após o recebimento de suas informações de contato e de inicialização, a Microsoft enviará uma chave de teste e uma chave de produção. Depois de ter adicionado a chave de teste ao registro e reiniciado o Player, sua loja online aparecerá no Player e você poderá testá-lo. Para obter informações sobre onde colocar sua chave de teste no registro, consulte [chaves e entradas do registro para uma loja online do tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md) ou [chaves do registro e entradas para uma loja online do tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).

Você deve testar todos os aspectos da sua loja online, incluindo sua interface do usuário e seu plug-in. Como parte do processo de teste, você deve executar os testes descritos em [testes de validação para lojas de música online do tipo 2](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Os repositórios do tipo 1 devem passar todos os testes de validação para os repositórios do tipo 2, além de alguns testes adicionais que são específicos para a experiência do tipo 1. Para obter informações sobre testes de validação do tipo 1, entre em contato com a equipe virtual dos serviços do Windows Media Player em mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Informações de contato

A tabela a seguir mostra as informações de contato que a Microsoft exige para sua loja online. Preencha o [formulário de informações de contato](contact-information-form-for-an-online-music-store.md) e envie-o para a equipe virtual dos serviços do Windows Media Player em mpsvctm@microsoft.com .



| Item                     | Descrição                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nome da Loja               | O nome da marca do seu repositório                                                            |
| Nome do Provedor            | O nome da empresa de rótulo de provedor/branco (se for diferente)                               |
| Localidade da loja             | As localidade do usuário do Windows em que sua loja deve ser exibida                                |
| Categoria do repositório           | Música, rádio, filme, TV, esportes, notícias, entretenimento de áudio e/ou outro (descreva) |
| Modelo de Compra           | Compra, aluguel, assinatura e/ou outro (por favor, descreva)                            |
| Idioma da loja           |                                                                                           |
| Armazenar nome (s) de contato    |                                                                                           |
| Armazenar email (s) de contato  |                                                                                           |
| Conta (s) do Passport MSFT | Isso é para possíveis indicações futuras em programas Beta e de desenvolvimento de parceiros.         |
| Endereço de envio         | Sem pedido Nas                                                                             |
| City                     |                                                                                           |
| Estado                    |                                                                                           |
| Código postal              |                                                                                           |
| País/Região           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contato da pesquisa           | Está tudo bem se entrarmos em contato com você sobre sua experiência com o programa no futuro?        |



 

## <a name="startup-information"></a>Informações de inicialização

Para cada região geográfica que seu armazenamento atenderá, envie à Microsoft um conjunto de informações de inicialização para seu repositório de teste, um conjunto de informações de inicialização para sua loja de produção e um conjunto de contas de validação.

O [formulário informações de inicialização do tópico para uma loja de música online](startup-information-form-for-an-online-music-store.md) contém duas cópias do formulário informações de inicialização e uma cópia do formulário contas de validação. Preencha os formulários e envie-os para a equipe virtual dos serviços do Windows Media Player em mpsvctm@microsoft.com .

A tabela a seguir descreve as informações de inicialização que a Microsoft exige para sua loja online.



| Item                                                                                                     | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL XML de informações de serviço (limite de 2048 caracteres)                                                              | A URL em que o Windows Media Player obtém seu [documento XML do serviceInfo](serviceinfo-document.md).                                                                                                                                         |
| Chave de serviço (ID exclusiva)                                                                                  | Uma cadeia de caracteres que identifica exclusivamente sua loja online. Você deve criar um para produção e outro para teste (por exemplo, "MyStore" e "MyStoreTest"). Observe que uma chave de serviço não é a mesma coisa que uma chave de teste.                        |
| Nome amigável (limite de 30 caracteres)                                                                       | O nome do seu repositório exibido no seletor de serviço do Windows Media Player.                                                                                                                                                        |
| URL da imagem do menu (limite de 2048 caracteres)                                                                    | A URL em que o Windows Media Player recupera o logotipo de 15 x 15 pixels que ele exibe no seletor de serviço.                                                                                                                                 |
| Comprar a URL de música (limite de 2048 caracteres)<br/> (Somente armazenamentos de música integrados)<br/>                | A URL usada pelos links "comprar CD" do Player e "comprar música online".                                                                                                                                                              |
| URL de compra da interface do usuário de 10 pés (limite de 2048 caracteres)<br/> (Somente armazenamentos de música integrados--opcional)<br/> | A URL usada pelos links "comprar CD" do Player e "comprar música online" no Windows XP Media Center Edition e no Windows Media Center no Windows Vista.                                                                              |
| Logotipo da loja (130W x 30h)<br/> (Anexe o arquivo PNG separadamente.)<br/>                              | O logotipo da loja exibido na dica de ferramenta que aparece quando o mouse está sobre a imagem procurar tudo. Esse logotipo deve ser um arquivo formatado em PNG e, preferencialmente, misturado para que ele possa ser ajustado para alterações de cores no Windows Media Player. |
| Procurar todas as imagens (108w x 108h)<br/> (Anexe o arquivo PNG separadamente.)<br/>                       | A breve descrição na dica de ferramenta que aparece quando o mouse está sobre sua imagem de procurar tudo.                                                                                                                                               |
| Armazenar texto de descrição (limite de 110 caracteres)                                                             | O texto que aparece na dica de ferramenta abaixo do texto de descrição da loja.                                                                                                                                                                        |
| Texto para hiperlink (limite de 45 caracteres)                                                                  | O logotipo da loja exibido na página procurar todas as lojas online. Ele deve ser um arquivo formatado em PNG e preferencialmente misturado para que ele possa ser ajustado para alterações de cores no Windows Media Player.                                           |



 

> [!Note]  
> A imagem 108 x 108 pixel procurar tudo é um requisito para o Windows Media Player 11 e posterior.

 

> [!Note]  
> No Windows Media Player 11 e posterior, os elementos ServiceTask2 e ServiceTask3 do documento XML do serviceInfo são ignorados. Para obter informações detalhadas sobre o documento XML do serviceInfo, consulte [documento do serviceInfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Contas de validação

Para concluir o processo de validação descrito na seção estágio de validação a seguir, a Microsoft requer cinco (5) contas de validação para cada tipo de conta que sua loja online oferece. Por exemplo, se você oferecer contas que diferenciam entre recursos e funcionalidades, como básico e Premium, a Microsoft precisará de cinco (5) contas de validação para cada tipo, para um total de dez (10) contas.

Envie o nome de usuário e a senha para cada conta de validação para mpsvctm@microsoft.com . Inclua também o nome de uma pessoa que a Microsoft pode contatar em relação às contas de validação. Essas contas serão usadas para validação mensal em andamento, portanto, inclua um processo para "recarregar" as contas. Um dos problemas mais comuns ocorre quando um armazenamento online falha ao fornecer crédito de compra suficiente para a Microsoft validar todos os cenários de compra. As contas devem permanecer ativas após a conclusão do processo de integração.

## <a name="validation-stage"></a>Estágio de validação

Durante o estágio de validação, a Microsoft verifica se os principais recursos da sua loja online funcionam corretamente. Para todos os repositórios (tipo 1 e tipo 2), a Microsoft executa os testes de verificação detalhados em [testes de validação para lojas de música online do tipo 2](validation-tests-for-type-2-online-music-stores.md). A Microsoft também executa alguns testes de validação adicionais para armazenamentos do tipo 1. Se você tiver dúvidas sobre o estágio de validação para repositórios do tipo 1, envie um email para mpsvctm@microsoft.com .

Durante o estágio de validação, a Microsoft faz duas passagens de validação. A primeira passagem se aplica à versão Release Candidate 1 (RC1) da sua loja online. Se a sua loja passar na validação RC1, você deverá bloqueá-la e não fazer nenhuma outra alteração. A Microsoft fará uma segunda passagem de validação em sua loja, mesmo se a sua loja passar na validação RC1.

Se a sua loja falhar em qualquer parte do passo de validação do RC1, você terá duas semanas para criar uma segunda versão Release Candidate (RC2), que a Microsoft validará durante o passo de validação do RC2.

Se a sua loja falhar em qualquer parte da validação do RC2, você deverá aguardar até a inicialização a seguir.

## <a name="test-and-production-keys"></a>Chaves de teste e de produção

Lembre-se de que, durante o estágio pendente, você enviou a Microsoft dois conjuntos de informações de inicialização: um para o repositório de teste e outro para sua loja de produção. Além disso, lembre-se de que a Microsoft enviou duas chaves: uma chave de teste e uma chave de produção.

A chave de teste é inteiramente para seu próprio uso. Quando a chave de teste estiver no registro, o Windows Media Player usará a URL do serviceInfo que você enviou para o seu repositório de teste.

Quando a chave de produção estiver no registro, o Windows Media Player usará a URL do serviceInfo que você enviou para sua loja de produção. A Microsoft usa sua chave de produção durante o estágio de validação. A Microsoft nunca usa sua chave de teste para validação.

Quando sua loja estiver ativa, o Windows Media Player usará a URL do serviceInfo que você enviou para sua loja de produção.

Como regra geral, seu repositório de teste deve ser o local onde você desenvolve seu serviço e faz alterações diárias. Sua loja de produção deve ser o local onde você mantém uma liberação estável do seu serviço.

## <a name="common-on-boarding-problems"></a>Problemas comuns de integração

Aqui estão alguns problemas comuns que podem fazer com que o armazenamento falhe no teste de validação.

-   Falha na transição de servidores de teste para servidores de produção. Isso leva a muitos problemas, como páginas ausentes, configurações de IIS e de segurança inválidas e contas de teste que não funcionam mais.
-   O link comprar (ou o link de compras) na área em execução é inválido. Isso pode fazer com que o armazenamento falhe na validação mesmo quando todo o resto estiver funcionando.
-   A equipe de validação da Microsoft testará vários cenários de compra, desde pequenas compras até compras muito grandes. Você deve fornecer uma maneira recarregáveis para que eles atuem como um consumidor em sua loja. Sua loja não poderá ser validada se a equipe de validação não tiver créditos de compra suficientes para validar todos esses cenários.

Para obter uma lista mais completa de problemas comuns de integração e perguntas frequentes compiladas pela equipe virtual de serviços do Windows Media Player, consulte [problemas comuns de integração para lojas de música online](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Kit de boas-vindas de lojas online](online-stores-welcome-kit.md)
</dt> </dl>

 

 





