---
title: Windows Guias de desenvolvedor da estrutura da faixa de Ribbon
description: os tópicos contidos nesta seção descrevem aspectos específicos do Windows estrutura da faixa de informações.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Windows Faixa de Ribbon, estrutura
- Faixa de Ribbon, estrutura
- Windows Faixa de guia, guias de desenvolvedor
- Faixa de guia, guias de desenvolvedor
- guias de desenvolvedor para a faixa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b30c5b2564dc918c6f9accfe5a5cb36a2d77222e3822a75a76332b1d3234cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850624"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Windows Guias de desenvolvedor da estrutura da faixa de Ribbon

os tópicos contidos nesta seção descrevem aspectos específicos do Windows estrutura da faixa de informações.

## <a name="basics"></a>Básico

[Criando um aplicativo de faixa de faixas](windowsribbon-stepbystep.md)

para o Windows estrutura da faixa de faixas consumir o arquivo de marcação da faixa de faixas, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. um compilador de marcação de faixa de medida dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação da faixa de faixas, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.

[migrando para a estrutura da faixa de Windows](ribbon-migration.md)

Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando da estrutura da faixa de ferramentas. Essa é uma maneira fácil e eficaz de modernizar e revitalize o aplicativo ao mesmo tempo em que também melhora a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.

[Noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md)

A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comando da estrutura da faixa de uma, um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.

## <a name="user-interface"></a>Interface do Usuário

[Especificando recursos de imagem da faixa de uma](windowsribbon-imageformats.md)

Como um sistema de apresentação de comando avançado, a estrutura da faixa de faixas foi projetada para dar suporte extensiva a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas. Todos os recursos de imagem são declarados na [marcação da faixa](windowsribbon-schema.md) de lista ou consultados de um aplicativo host da faixa de Ribbon.

para Windows 8 e posteriores, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network graphics) com transparência.

para o Windows 7 e anterior, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado em Windows.

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)

Os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout que são impostas pela estrutura da faixa de opções e com base em uma combinação de comportamentos padrão e modelos de layout (ambos definidos pelo Framework e personalizados), conforme declarado na marcação da faixa de opções. Essas regras definem os comportamentos de layout adaptável da estrutura da faixa de opção que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opção em tempo de execução.

[Trabalhando com galerias](ribbon-controls-galleries.md)

A estrutura da faixa de tipos fornece aos desenvolvedores um modelo robusto e consistente para o gerenciamento de conteúdo dinâmico em uma variedade de controles baseados em coleção. Ao adaptar e reconfigurar a interface do usuário da faixa de opções (IU), esses controles dinâmicos permitem que a estrutura responda à interação do usuário tanto no aplicativo host quanto na faixa de opções e forneça a flexibilidade para lidar com vários ambientes de tempo de execução.

[Exibindo guias contextuais](ribbon-contextualtabs.md)

Em um aplicativo do Framework da faixa de das, uma guia contextual é um controle de [guia](windowsribbon-controls-tab.md) oculto que é exibido na linha da guia quando um objeto no espaço de trabalho do aplicativo, como uma imagem, é selecionado ou realçado.

[Reconfiguração da faixa de modo com modos de aplicativo](ribbon-applicationmodes.md)

A estrutura da faixa de faixas é compatível com a reconfiguração dinâmica e a exposição de elementos principais da interface do usuário da faixa de medida (IU) em tempo de execução, com base no estado do aplicativo (também conhecido como contexto). Declarados e associados a elementos específicos na marcação, os vários Estados com suporte de um aplicativo são chamados de modos de aplicativo.

[Personalizando cores da faixa de das](ribbon-color.md)

A estrutura da faixa de faixas expõe um conjunto de propriedades de cores que permite a um aplicativo personalizar a aparência de vários elementos da interface do usuário da faixa de faixas em tempo de execução.

[Exibindo a faixa de faixas](ribbon-visibility.md)

A estrutura da faixa de forma expõe um conjunto de propriedades que permite que um aplicativo especifique como a interface do usuário da faixa de forma (IU) é exibida em tempo de execução.

## <a name="management"></a>Gerenciamento

[Estado da faixa de medida persistente](ribbon-statepersistence.md)

a estrutura de Windows Ribon (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.

[Escutando eventos da faixa de das](listening-for-ribbon-events.md)

a estrutura da faixa de faixas usa a infraestrutura de [rastreamento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de forma de seu aplicativo.

## <a name="markup-compiler"></a>Compilador de marcação

[Compilando marcação da faixa de medida](windowsribbon-intentcl.md)

Para que a estrutura da faixa de faixas consuma o arquivo de [marcação da faixa de faixas](windowsribbon-schema.md) , o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. um compilador de marcação dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.

[Compreendendo as mensagens do compilador de marcação](windowsribbon-compilationerrors.md)

o compilador de marcação da faixa de opções da Windows (ribbon), compilador de comando de interface do usuário (UICC.exe), valida a marcação da faixa de opções em relação ao esquema da faixa e um conjunto adicional de regras definidas pela estrutura da faixa de opções.

 

 