---
title: Definindo um novo caractere
description: Definindo um novo caractere
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1f3d9aee78893ebc4796781947be92366baa10b9ad1e123a73121df24646ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963096"
---
# <a name="defining-a-new-character"></a>Definindo um novo caractere

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para definir um novo caractere, execute o Editor de Caracteres do Agente. Se você tiver um arquivo de caracteres existente carregado, escolha o **comando Novo** **no** menu Arquivo. Isso exibe um submenu de opções. Se você criar um caractere para seu próprio uso, escolha **Caractere Personalizado**. Se você quiser criar um caractere que possa ser usado como um caractere padrão do Agent, escolha **Caractere Padrão**. Isso pré-configurará o editor com todos os nomes de animação e atribuições de estado de animação necessários, bem como definirá a opção Suporte ao Conjunto de **Animação** Padrão. Da mesma forma, se você escolher Office de Assistente, o editor será pré-configurado com os nomes de animação e a atribuição de estado de animação necessárias para um caractere Office Assistente. Essa ação seleciona o **ícone Caractere** na árvore e exibe suas páginas de propriedades no lado direito da janela. As seções a seguir descrevem como definir as propriedades do caractere e como criar animações para o caractere.

### <a name="setting-your-characters-general-information"></a>Definindo as informações gerais do caractere

Para começar a definir um caractere, insira o nome do caractere na **caixa** de texto Nome (máximo de 32 caracteres). Como o Microsoft Agent usa o nome para permitir que os usuários acessem o caractere, especifique um nome amigável. Fornecer um nome que possa ser pronunciado usando a ortografia convencional ou você poderá desabilitar a entrada de fala para o caractere. Você também pode especificar uma breve descrição opcional (256 caracteres) para o caractere na caixa de texto Descrição. O servidor expõe o que você inserir na caixa de texto Descrição para aplicativos cliente.

Você também pode armazenar seus próprios dados como parte do caractere usando o campo ExtraData. Você pode usar essa funcionalidade para incluir informações especiais sobre seu caractere ou outros dados. Depois de compiladas com o Editor de Caracteres, essas informações podem ser acessadas usando a propriedade ExtraData em tempo de executar quando o caractere é carregado.

Você pode definir o nome, a descrição e as informações de dados extras do caractere com base na configuração de ID de idioma do caractere. Para definir esses dados para outro idioma, selecione Idioma e insira o texto. Você também deve ter as páginas de código de idioma instaladas no sistema em que você cria o arquivo de caracteres. Caso não faça isso, as configurações de idioma apropriadas não serão incluídas no arquivo de caracteres compilado. Você não precisa fornecer informações em outros idiomas. Se essas propriedades são consultadas em runtime usando a API do Agent e não há configurações específicas para esse idioma, as configurações em inglês (Padrão) são retornadas.

### <a name="setting-your-characters-output-options"></a>Definindo as opções de saída do caractere

Se você definir a opção Suporte ao Conjunto de Animação Padrão, o Editor de Caracteres verificará se você incluiu todas as animações e atribuições de estado de animação necessárias para um caractere padrão ao tentar criar o caractere. Se algo estiver faltando, uma caixa de mensagem lista os elementos ausentes. Para obter detalhes sobre o conjunto de animação padrão, consulte [**Projetando caracteres para o Microsoft Agent.**](designing-characters-for-microsoft-agent.md)

Para a saída falada do caractere, o Microsoft Agent fornece a opção de uma voz TTS (texto em fala) sintetizada ou uma voz que usa arquivos de som gravados. Se você quiser usar uma voz sintetizada, marque a opção Usar Fala Sintetizada para Saída de Voz. Isso adicionará uma página Voz para selecionar as características da voz. Escolha a página Voz e use os controles na página para selecionar uma voz, velocidade e tom de qualquer mecanismo TTS compatível que você tenha instalado. O intervalo dos parâmetros de voz que você pode selecionar depende dos mecanismos TTS. Se você ainda não tiver instalado um mecanismo TTS, a lista de IDs de Voz estará vazia. Você deve ter um mecanismo TTS instalado antes de definir as configurações de voz do caractere no Editor de Caracteres do Agente.

Se você planeja usar um mecanismo TTS para a saída do caractere, também deve instalar esse mecanismo no sistema do usuário. Se você selecionar uma voz com base em um mecanismo TTS específico, mas o usuário tiver um mecanismo TTS diferente instalado, o servidor tentará corresponder à voz com base nas características definidas no Editor de Caracteres do Agente.

Se você planeja usar arquivos de som gravados (. Arquivos WAV) para a saída falada do caractere, você não precisa verificar a opção Usar Fala Sintetizada para Saída de Voz. Em vez disso, você precisará registrar os arquivos de áudio de saída falados separadamente e carregá-los do código do aplicativo.

A opção **Usar Balão** do Word permite que você determine se deseja dar suporte a um balão de palavra para seu caractere. Esse recurso também pode ser definido em tempo de executar.

Quando a **opção Usar Balão do Word** estiver marcada, você poderá acessar a página Balão do **Word.** As opções na página **Balão do Word** permitem alterar as características padrão do balão de palavras. A **configuração Caracteres** por Linha permite que você defina a largura do balão com base no número médio de caracteres por linha. Você pode definir a altura padrão com base em um número fixo de linhas que deseja exibir ao mesmo tempo ou dimensionado automaticamente para o texto que você fornece no [**método Speak.**](speak-method.md) Você também pode definir se o balão é ocultado automaticamente depois que um método **Speak** é concluído e se o balão exibe automaticamente ou "acompanha" palavras para a configuração de velocidade de saída de fala do caractere.

A **página Balão do** Word também permite definir a fonte padrão para o balão de palavras do caractere e as cores de exibição do balão. No entanto, esteja ciente de que os usuários podem substituir suas configurações de fonte de balão de palavras usando a folha de propriedades do Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Definindo o identificador do caractere

Cada caractere requer um GUID (identificador exclusivo). O servidor usa o identificador para diferenciar caracteres. Quando você cria um novo caractere, o Editor cria automaticamente um novo identificador para o caractere. Você precisará alterar o identificador de um caractere somente se tiver copiado o arquivo de definição de caractere de outro caractere ou se quiser diferenciar intencionalmente um caractere de uma versão anterior. Para alterar o identificador de um caractere, clique no botão Novo GUID e o Editor gerará um novo identificador.

 

 




