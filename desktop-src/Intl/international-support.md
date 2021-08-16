---
description: esta seção descreve as tecnologias em Windows que permitem que você ofereça suporte a várias culturas e linguagens escritas do marketplace internacional em seu aplicativo Microsoft Win32 baseado em C ou C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internacionalização para aplicativos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78f4831390ffc31a5f3290f0784d32c3aa1044863c708e6e0329225519c2cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147539"
---
# <a name="internationalization-for-windows-applications"></a>Internacionalização para aplicativos do Windows

(Anteriormente intitulado "suporte internacional")

esta seção descreve as tecnologias em Windows que permitem que você ofereça suporte a várias culturas e linguagens escritas do marketplace internacional em seu aplicativo Microsoft Win32 baseado em C ou C++.

Windows tornou-se uma plataforma essencial para os clientes em todo o mundo. Os usuários internacionais esperam soluções que são adaptadas para suas linguagens e regiões em todo o mundo. Nesta seção, você encontrará as informações necessárias para desenvolver soluções multilíngües, Multicultura e multissite. o suporte internacional interno do Windows permite que você implemente muitos cenários com menos sobrecarga de engenharia do que nunca.

O desenvolvimento de aplicativos preparados para o mundo requer o uso de vários serviços e ferramentas. o Windows contém recursos que permitem desenvolver soluções que:

- Dê suporte a diferentes necessidades específicas de idioma e localidade de usuários em todo o mundo (incluindo suporte a texto especializado, comportamento de classificação, formatação de data e hora e layouts de teclado). (Para obter mais informações, consulte [centro de conhecimento de suporte ao idioma nacional](./national-language-support-reference.md).)
- São globalizados (podem ser implantados em todo o mundo a partir de uma única imagem binária) e podem ser localizados (capazes de ser adaptados para mercados locais específicos). (para obter mais informações, consulte [Interface de Usuário Multilíngue](./multilingual-user-interface.md).)
- Exibir fontes e texto internacionais e permitir que os usuários especifiquem a fonte que desejam. (Para obter mais informações, consulte [suporte a scripts e fontes no Windows](/globalization/input/font-support).)
- Permitir que o usuário insira caracteres complexos e símbolos com um teclado padrão.
- Fornecer suporte para vários idiomas escritos diferentes por meio de Unicode e conjuntos de caracteres tradicionais.
- Descubra a entrada de idioma por um usuário e personalize a experiência do usuário fornecida pelo seu aplicativo. (para obter mais informações, consulte [escrevendo aplicativos preparados para o mundo em Windows: serviços lingüísticos estendidos no Windows](./using-extended-linguistic-services.md).)

## <a name="in-this-section"></a>Nesta seção

As seguintes tecnologias de suporte internacional estão documentadas nesta seção. Eles são listados com alguns cenários importantes para os quais podem ser usados.

- [Introdução com o desenvolvimento de Windows internacional](getting-started-with-international-development.md)

    Descreve como começar a criar aplicativos preparados para o mundo e fornece um tutorial ilustrando uma tarefa comum na escrita de software global.

    Cenários comuns:

    - Determine um caminho a ser levado para aprender a desenvolver software internacional.
    - descubra as tecnologias de internacionalização disponíveis no SDK (Software Development Kit) do Microsoft Windows.
    - Siga um tutorial que usa um aplicativo multilíngue existente e adiciona suporte para idiomas adicionais.

- [Serviços de globalização](globalization-services.md)

    Descreve os [Els (serviços lingüísticos estendidos)](extended-linguistic-services.md), que permitem que você descubra a linguagem na qual o texto e a entrada do usuário são gravados, e o [NLS (suporte ao idioma nacional)](national-language-support.md), que permite que um aplicativo use informações de localidade para exibir informações sensíveis à cultura (como hora, datas e moeda) e as cadeias de caracteres de classificação adequadas.

    Cenários comuns:

    - Descubra o idioma da entrada do usuário, para que o conteúdo da ajuda possa ser exibido em um idioma compreensível.
    - Descubra o script usado no texto a ser exibido. Se ele for chinês simplificado ou tradicional, ofereça ao usuário a opção de fazer com que o texto seja transliterado de um para o outro.
    - Permitir que o usuário selecione uma localidade (uma coleção de informações de preferência do usuário relacionadas à linguagem).
    - Exiba horas, datas, informações de calendário, moeda e muitos outros objetos dependentes de cultura em linguagens e formatos apropriados.
    - Classificar cadeias de caracteres na ordem esperada pelo usuário de uma determinada localidade.

- [Gerenciador de métodos de entrada](input-method-manager.md)

    Descreve a tecnologia usada por um aplicativo para se comunicar com um IME (editor de método de entrada). O IME permite que os usuários de computador insiram caracteres e símbolos complexos usando um teclado padrão.

    Cenário comum:

    - Permitir que o usuário use um teclado padrão para inserir caracteres em japonês kanji.

- [Fontes internacionais e exibição de texto](international-fonts-and-text-display.md)

    descreve o suporte fornecido pela plataforma de Windows para fontes internacionais, texto internacional e tipografia fina.

    Cenários comuns:

    - Permitir que o usuário selecione fontes internacionais com base no conjunto de caracteres.
    - Exibir texto internacional.
    - Processar scripts complexos, incluindo renderização bidirecional, shaping contextual e ligaduras (Uniscribe).
    - Permitir um alto grau de controle para a tipografia fina (Uniscribe).

- [Interface do Usuário Multilíngue](multilingual-user-interface.md)

    Descreve como os aplicativos podem separar recursos dependentes de idioma do código neutro de idioma para idiomas de interface do usuário com suporte.

    Cenários comuns:

    - Crie imagens de implantação única regionais ou mundiais de um aplicativo.
    - Localize uma solução atualizando os recursos do aplicativo sem alterar para o código-fonte do aplicativo.
    - Permitir que os usuários alternem de um idioma da interface do usuário para outro em tempo de execução.

- [Unicode e conjuntos de caracteres](unicode-and-character-sets.md)

    Descreve como os aplicativos podem aproveitar o Unicode, o padrão mundial de codificação de caracteres que usa valores de código de 16 bits para representar todos os caracteres usados na computação moderna, incluindo símbolos técnicos e caracteres especiais usados na publicação.

    Cenários comuns:

    - Dê suporte a vários idiomas diferentes do Marketplace internacional por meio de Unicode.
    - Converta caracteres Unicode de e para outros conjuntos de caracteres, quando necessário.

- [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md)

    Fornece informações sobre considerações de segurança relacionadas aos recursos de suporte de desenvolvimento internacional.

    As informações de segurança pertencem a todos os cenários.

## <a name="related-international-technologies"></a>Tecnologias internacionais relacionadas

O suporte ao desenvolvimento internacional também está disponível para aplicativos escritos em código gerenciado. se estiver desenvolvendo para o .NET Framework, você precisará de alguns ou de todos eles:

- O [namespace System. Globalization](/dotnet/api/system.globalization) contém classes que definem informações relacionadas à cultura e fornecem funções de globalização avançadas.
- O [namespace System. Text](/dotnet/api/system.text) contém classes que representam codificações de caracteres, convertem blocos de caracteres e manipulam e formatam objetos de cadeia de caracteres.
