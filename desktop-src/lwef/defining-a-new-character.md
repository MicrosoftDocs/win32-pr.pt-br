---
title: Definindo um novo caractere
description: Definindo um novo caractere
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586312ac9d913a27d2df0be112cbcf92c47f4fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916392"
---
# <a name="defining-a-new-character"></a>Definindo um novo caractere

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para definir um novo caractere, execute o editor de caracteres do agente. Se você tiver um arquivo de caractere existente carregado, escolha o comando **novo** no menu **arquivo** . Isso exibe um submenu de opções. Se você criar um caractere para seu próprio uso, escolha **caractere personalizado**. Se você quiser criar um caractere que possa ser usado como um caractere padrão de agente, escolha **caractere padrão**. Isso configurará previamente o editor com todos os nomes de animação e atribuições de estado de animação necessários, bem como definirá a opção **oferece suporte ao conjunto de animações padrão** . Da mesma forma, se você escolher o caractere assistente do Office, o editor será pré-configurado com os nomes de animação e a atribuição de estado de animação necessários para um caractere do assistente do Office. Essa ação seleciona o ícone de **caractere** na árvore e exibe suas páginas de propriedades no lado direito da janela. As seções a seguir descrevem como definir as propriedades de seu caractere e como criar animações para o caractere.

### <a name="setting-your-characters-general-information"></a>Definindo as informações gerais do seu caractere

Para começar a definir um caractere, insira o nome do caractere na caixa de texto **nome** (máximo de 32 caracteres). Como o Microsoft Agent usa o nome para permitir que os usuários acessem o caractere, especifique um nome amigável para o usuário. Forneça um nome que possa ser pronunciado usando a grafia convencional ou você pode desabilitar a entrada de fala para o caractere. Você também pode especificar uma descrição opcional curta (256 caracteres) para seu caractere na caixa de texto descrição. O servidor expõe o que você insere na caixa de texto descrição para aplicativos cliente.

Você também pode armazenar seus próprios dados como parte do seu caractere usando o campo ExtraData. Você pode usar essa capacidade para incluir informações especiais sobre seu caractere ou outros dados. Depois de compilado com o editor de caracteres, essas informações podem ser acessadas usando a propriedade ExtraData em tempo de execução quando o caractere é carregado.

Você pode definir o nome, a descrição e as informações de dados adicionais do caractere com base na configuração de ID de idioma do caractere. Para definir esses dados para outro idioma, selecione idioma e insira o texto. Você também deve ter as páginas de código do idioma instaladas no sistema que cria o arquivo de caractere. Se você não tiver as configurações de idioma apropriadas, elas não serão incluídas no arquivo de caractere compilado. Você não precisa fornecer informações em outras linguagens. Se essas propriedades forem consultadas em tempo de execução usando a API do agente e não houver configurações específicas para esse idioma, as configurações em inglês (padrão) serão retornadas.

### <a name="setting-your-characters-output-options"></a>Definindo as opções de saída de seu caractere

Se você definir a opção oferece suporte ao conjunto de animações padrão, o editor de caracteres verificará se você incluiu todas as animações necessárias e as atribuições de estado de animação para um caractere padrão quando tentar criar o caractere. Se algo estiver faltando, uma caixa de mensagem listará os elementos ausentes. Para obter detalhes sobre o conjunto de animações padrão, consulte [**criando caracteres para o Microsoft Agent**](designing-characters-for-microsoft-agent.md).

Para a saída falada de seu caractere, o Microsoft Agent fornece a opção de uma voz sintetizada, de conversão de texto em fala (TTS) ou uma voz que usa arquivos de som gravados. Se você quiser usar uma voz sintetizada, marque a opção usar fala sintetizada para saída de voz. Isso adicionará uma página de voz para selecionar as características da voz. Escolha a página de voz e use os controles na página de ti para selecionar uma voz, uma velocidade e um tom de quaisquer mecanismos de TTS compatíveis que você tenha instalado. O intervalo dos parâmetros de voz que você pode selecionar depende dos mecanismos de TTS. Se você ainda não tiver instalado um mecanismo de TTS, a lista ID de voz estará vazia. Você deve ter um mecanismo de TTS instalado antes de definir as configurações de voz do caractere no editor de caracteres do agente.

Se você planeja usar um mecanismo de TTS para a saída de seu caractere, você também deve instalar esse mecanismo no sistema do usuário. Se você selecionar uma voz com base em um mecanismo de TTS específico, mas o usuário tiver um mecanismo de TTS diferente instalado, o servidor tentará corresponder à voz com base nas características que você definiu no editor de caracteres do agente.

Se você planeja usar arquivos de som gravados (. Arquivos WAV) para a saída falada de seu caractere, você não precisa marcar a opção usar fala sintetizada para saída de voz. Em vez disso, você precisará gravar os arquivos de áudio de saída falados separadamente e carregá-los do código do aplicativo.

A opção usar **balão de palavras** permite que você determine se deseja dar suporte a um balão de palavras para seu caractere. Esse recurso também pode ser definido em tempo de execução.

Quando a opção **usar balão de palavras** estiver marcada, você poderá acessar a página de **balão do Word** . As opções na página **balão do Word** permitem que você altere as características padrão de seu balão de palavra. A configuração de **caracteres por linha** permite que você defina a largura do balão com base no número médio de caracteres por linha. Você pode definir a altura padrão com base em um número fixo de linhas que deseja exibir de uma vez ou automaticamente dimensionada para o texto que você fornecer no método [**Speak**](speak-method.md) . Você também pode definir se o balão será ocultado automaticamente depois que um método de **fala** for concluído e se o balão exibirá automaticamente ou "ritmos" palavras para a configuração de velocidade de saída de fala do caractere.

A página **balão de palavras** também permite que você defina a fonte padrão para o balão de palavras do caractere e as cores de exibição do balão. No entanto, lembre-se de que os usuários podem substituir as configurações de fonte do balão de palavras usando a folha de propriedades do Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Definindo o identificador de seu caractere

Cada caractere requer um GUID (identificador exclusivo). O servidor usa o identificador para diferenciar caracteres. Quando você cria um novo caractere, o editor cria automaticamente um novo identificador para seu caractere. Você precisará alterar o identificador de um caractere somente se tiver copiado o arquivo de definição de caractere de outro caractere ou se desejar diferenciar um caractere de uma versão anterior. Para alterar o identificador de um caractere, clique no botão novo GUID e o editor irá gerar um novo identificador.

 

 




