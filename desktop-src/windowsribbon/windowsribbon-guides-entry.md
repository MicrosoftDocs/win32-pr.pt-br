---
title: Guias de desenvolvedor do Windows Ribbon Framework
description: Os tópicos contidos nesta seção descrevem aspectos específicos do Windows Ribbon Framework.
ms.assetid: 87434a15-ba13-4c6f-a814-49ae2349bfa2
keywords:
- Faixa de Ribbon do Windows, estrutura
- Faixa de Ribbon, estrutura
- Faixa de-se do Windows, guias de desenvolvedor
- Faixa de guia, guias de desenvolvedor
- guias do desenvolvedor para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b6e88045efdd31384d99370fdd9bb9cb264598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084801"
---
# <a name="windows-ribbon-framework-developer-guides"></a>Guias de desenvolvedor do Windows Ribbon Framework

Os tópicos contidos nesta seção descrevem aspectos específicos do Windows Ribbon Framework.

## <a name="basics"></a>Noções básicas

[Criando um aplicativo de faixa de faixas](windowsribbon-stepbystep.md)

Para que o Windows Ribbon Framework consuma o arquivo de marcação da faixa de faixas, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. Um compilador de marcação de faixa de medida dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação da faixa de faixas, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.

[Migrando para o Windows Ribbon Framework](ribbon-migration.md)

Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando da estrutura da faixa de ferramentas. Essa é uma maneira fácil e eficaz de modernizar e revitalize o aplicativo ao mesmo tempo em que também melhora a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.

[Noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md)

A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comando da estrutura da faixa de uma, um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.

## <a name="user-interface"></a>Interface do Usuário

[Especificando recursos de imagem da faixa de uma](windowsribbon-imageformats.md)

Como um sistema de apresentação de comando avançado, a estrutura da faixa de faixas foi projetada para dar suporte extensiva a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas. Todos os recursos de imagem são declarados na [marcação da faixa](windowsribbon-schema.md) de lista ou consultados de um aplicativo host da faixa de Ribbon.

Para o Windows 8 e posterior, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network Graphics) com transparência.

Para o Windows 7 e versões anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado no Windows.

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

O Windows Ribon Framework (faixa de opções) fornece a capacidade de preservar o estado de uma variedade de configurações de usuário e preferências entre sessões de aplicativos.

[Escutando eventos da faixa de das](listening-for-ribbon-events.md)

A estrutura da faixa de faixas usa a infraestrutura do [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de forma do aplicativo.

## <a name="markup-compiler"></a>Compilador de marcação

[Compilando marcação da faixa de medida](windowsribbon-intentcl.md)

Para que a estrutura da faixa de faixas consuma o arquivo de [marcação da faixa de faixas](windowsribbon-schema.md) , o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário. Um compilador de marcação dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Microsoft Windows (7,0 ou posterior) para essa finalidade. Além de compilar a versão binária da marcação, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.

[Compreendendo as mensagens do compilador de marcação](windowsribbon-compilationerrors.md)

O compilador de marcação do Windows Ribbon Framework (faixa de opções), o compilador de comando da interface do usuário (UICC.exe), valida a marcação da faixa de opções em relação ao esquema da faixa e um conjunto adicional de regras definidas pela estrutura da faixa de opções.

 

 