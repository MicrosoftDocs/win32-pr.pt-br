---
title: Windows Guias do desenvolvedor da Estrutura de Faixa de Opções
description: Os tópicos contidos nesta seção descrevem aspectos específicos da estrutura Windows Faixa de Opções.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows Faixa de opções, estrutura
- Faixa de opções, estrutura
- Windows Faixa de opções, guias de desenvolvedor
- Faixa de opções, guias de desenvolvedor
- guias de desenvolvedor para Windows faixa de opções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850624"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows Guias do desenvolvedor da Estrutura de Faixa de Opções

Os tópicos contidos nesta seção descrevem aspectos específicos da estrutura Windows Faixa de Opções.

## <a name="basics"></a>Básico

[Criando um aplicativo de faixa de opções](windowsribbon-stepbystep.md)

Para que a Windows faixa de opções consuma o arquivo de marcação faixa de opções, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. Um compilador de marcação da Faixa de Opções dedicado, o UICC (Compilador de Comando da Interface do Usuário), está incluído com o SDK (Software Development Kit) do Microsoft Windows (7.0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação Faixa de Opções, o UICC gera um arquivo de título de definição de ID (.h) que expõe todos os elementos de marcação para o aplicativo host da Faixa de Opções e um arquivo de recurso (.rc) usado para vincular recursos de imagem e cadeia de caracteres ao aplicativo host no momento da compilação.

[Migrando para a estrutura Windows faixa de opções](ribbon-migration.md)

Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário (interface do usuário) rica, dinâmica e controlada por contexto do sistema de comando da estrutura de faixa de opções. Essa é uma maneira fácil e eficaz de modernizar e desabilizar o aplicativo, além de melhorar a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.

[Noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md)

A separação da lógica da apresentação é a filosofia de design que inspirado o sistema de apresentação de comando da estrutura ribbon – um sistema baseado em um padrão de design em que a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.

## <a name="user-interface"></a>Interface do Usuário

[Especificando recursos de imagem da faixa de opções](windowsribbon-imageformats.md)

Como um sistema de apresentação de comando rico, a estrutura ribbon foi projetada para dar suporte extensiva aos recursos de imagem em toda a interface do usuário da Faixa de Opções. Todos os recursos de imagem são declarados na [marcação faixa de opções](windowsribbon-schema.md) ou consultados de um aplicativo host da Faixa de Opções.

Para Windows 8 posteriores, a estrutura ribbon dá suporte aos seguintes formatos gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Gráficos de Rede Portátil) com transparência.

Por Windows 7 e anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado Windows.

[Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)

Os controles hospedados na barra de comandos da faixa de opções estão sujeitos às regras de layout impostas pela estrutura da Faixa de Opções e com base em uma combinação de comportamentos padrão e modelos de layout (definidos por estrutura e personalizados), conforme declarado na marcação faixa de opções. Essas regras definem os comportamentos de layout adaptável da estrutura da Faixa de Opções que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opções em tempo de corrida.

[Trabalhando com galerias](ribbon-controls-galleries.md)

A estrutura ribbon fornece aos desenvolvedores um modelo robusto e consistente para gerenciar conteúdo dinâmico em uma variedade de controles baseados em coleção. Ao adaptar e reconfigurar a interface do usuário da Faixa de Opções, esses controles dinâmicos permitem que a estrutura responda à interação do usuário no aplicativo host e na faixa de opções em si e forneça a flexibilidade para lidar com vários ambientes de tempo de run time.

[Exibindo guias contextuais](ribbon-contextualtabs.md)

Em um aplicativo de estrutura da Faixa de Opções, uma guia contextual é um controle [Tab](windowsribbon-controls-tab.md) oculto que é exibido na linha da guia quando um objeto no workspace do aplicativo, como uma imagem, é selecionado ou realçado.

[Reconfigurando a faixa de opções com modos de aplicativo](ribbon-applicationmodes.md)

A estrutura da Faixa de Opções dá suporte à reconfiguração dinâmica e à exposição de elementos principais da interface do usuário da Faixa de Opções em tempo de operação, com base no estado do aplicativo (também conhecido como contexto). Declarados e associados a elementos específicos na marcação, os vários estados com suporte de um aplicativo são chamados de modos de aplicativo.

[Personalização das cores da faixa de opções](ribbon-color.md)

A estrutura da Faixa de Opções expõe um conjunto de propriedades de cores que permitem que um aplicativo personalize a aparência de vários elementos de interface do usuário da Faixa de Opções em tempo de executar.

[Exibindo a faixa de opções](ribbon-visibility.md)

A estrutura da Faixa de Opções expõe um conjunto de propriedades que permitem que um aplicativo especifique como a interface do usuário da Faixa de Opções é exibida em tempo de operação.

## <a name="management"></a>Gerenciamento

[Persistindo o estado da faixa de opções](ribbon-statepersistence.md)

A Windows framework Windows (Faixa de Opções) fornece a capacidade de preservar o estado de uma variedade de configurações e preferências do usuário entre as sessões do aplicativo.

[Escutando eventos da faixa de opções](listening-for-ribbon-events.md)

A estrutura ribbon usa a infraestrutura [ETW (Rastreamento](../etw/event-tracing-portal.md) de Eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de opções do aplicativo.

## <a name="markup-compiler"></a>Compilador de marcação

[Compilando marcação de faixa de opções](windowsribbon-intentcl.md)

Para que a estrutura da Faixa de Opções consuma o arquivo de marcação [faixa](windowsribbon-schema.md) de opções, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. Um compilador de marcação dedicado, o UICC (Compilador de Comando da Interface do Usuário), está incluído com o SDK (Software Development Kit) do Microsoft Windows (7.0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação, o UICC gera um arquivo de título de definição de ID (.h) que expõe todos os elementos de marcação para o aplicativo host da Faixa de Opções e um arquivo de recurso (.rc) usado para vincular recursos de imagem e cadeia de caracteres ao aplicativo host no momento da compilação.

[Noções básicas sobre mensagens do compilador de marcação](windowsribbon-compilationerrors.md)

O compilador de marcação Windows Ribbon Framework (Ribbon), o compilador de comando da interface do usuário (UICC.exe), valida a marcação faixa de opções em relação ao esquema da Faixa de Opções e a um conjunto adicional de regras definido pela estrutura da Faixa de Opções.

 

 