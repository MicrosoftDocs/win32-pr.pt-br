---
description: Este tópico define os termos que são importantes ao trabalhar com a funcionalidade NLS.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: Terminologia do NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a86808d31cb034e7ad29e4580b8f201ad3c9a6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663381"
---
# <a name="nls-terminology"></a>Terminologia do NLS

Este tópico define os termos que são importantes ao trabalhar com a funcionalidade NLS.

## <a name="locale-and-language-terms"></a>Termos de localidade e idioma

A tabela a seguir resume os termos de localidade e idioma. Consulte também [localidades e idiomas](locales-and-languages.md).



|                          | Grupo de idiomas                                                                                                                                                                                                                                                                   | Idioma para programas não Unicode                                                                                                                                                                                                                | Padrões e formatos                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalidade**              | Fornece todos os layouts de teclado, IMEs (Input Method Editors), fontes TrueType, links de fonte, LPKs (arquivos de pacote de licença), fontes de bitmap e tabelas de conversão de página de código necessárias para o sistema operacional para um grupo de idiomas. Portanto, o afeta todas as outras configurações nesta lista. | Determina quais fontes de bitmap e as páginas de código OEM, ANSI e Macintosh são padrões para o sistema operacional. Esse idioma afeta apenas os aplicativos que não são totalmente Unicode. Antes do Windows XP, esse idioma era chamado de "localidade do sistema". | Determina quais configurações são usadas para formatar datas, horas, moedas e números como um padrão para cada usuário. Também determina a ordem de classificação para classificar o texto. Antes do Windows XP, os padrões e os formatos eram chamados de "localidade do usuário". |
| **Primeiro conjunto**            | Instalação                                                                                                                                                                                                                                                                     | Instalação                                                                                                                                                                                                                                     | Instalação                                                                                                                                                                                                                            |
| **Como os usuários podem alterar** | Opções regionais (item do painel de controle)<br/> **Windows XP:** Opções regionais e de idioma<br/> (somente administradores)<br/>                                                                                                                                       | Opções regionais (item do painel de controle)<br/> **Windows XP:** Opções regionais e de idioma<br/> (somente administradores)<br/>                                                                                                       | Opções regionais (item do painel de controle)<br/> **Windows XP:** Opções regionais e de idioma<br/>                                                                                                                               |
| **Padrão**              | Europa Ocidental e Estados Unidos e grupo de idiomas necessários para exibir o idioma de uma versão localizada.                                                                                                                                                                         | Idioma da versão localizada.                                                                                                                                                                                                                   | Idioma do sistema operacional localizado.                                                                                                                                                                                                 |
| **Função**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Localidade do thread                                                                                                                                                 | Idioma de entrada                                                                                            | Idioma da interface do usuário padrão do sistema                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalidade**              | Determina as configurações que são usadas para formatar datas, horas, moedas e números grandes para um thread. Também determina a ordem de classificação para classificar o texto. | Consiste em um idioma e um método de entrada.                                                             | Determina o idioma padrão de menus e caixas de diálogo, mensagens, arquivos INF (informações de instalação) e arquivos de ajuda.<br/> **Windows Vista e posterior:** Conhecido como idioma de instalação. Desempenha uma função mais limitada, amplamente substituída por linguagens de interface do usuário preferenciais do sistema.<br/> Para obter mais informações, consulte [User Interface Language Management](user-interface-language-management.md)<br/> |
| **Primeiro conjunto**            | Padrões e formatos padrão                                                                                                                              | Instalação                                                                                              | Instalação                                                                                                                                                                                                                                                                                                                                                                                   |
| **Como os usuários podem alterar** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Opções regionais (item do painel de controle)<br/> **Windows XP:** Opções regionais e de idioma<br/> | Não                                                                                                                                                                                                                                                                                                                                                                                             |
| **Padrão**              | Padrões e formatos                                                                                                                                         | Idioma da versão localizada com o método de entrada padrão.                                                  | Idioma da versão localizada.                                                                                                                                                                                                                                                                                                                                                                 |
| **Função**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Idioma da interface do usuário do sistema, idiomas preferenciais da interface do usuário                                                                                                                                                                  | Idioma da interface do usuário, idiomas de interface do usuário preferenciais                                                                                                                                               | Linguagens de interface do usuário preferencial de thread                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalidade**              | Determine o idioma de menus e caixas de diálogo, mensagens, arquivos INF e arquivos de ajuda para o sistema operacional. Para obter mais informações, consulte [User Interface Language Management](user-interface-language-management.md). | Determine o idioma de menus e caixas de diálogo, mensagens e arquivos de ajuda para o usuário. Para obter mais informações, consulte [User Interface Language Management](user-interface-language-management.md). | **Windows Vista e posterior:** Especifique os idiomas preferenciais para threads de aplicativo. Para obter mais informações, consulte [User Interface Language Management](user-interface-language-management.md). |
| **Primeiro conjunto**            | Padrão para NULL                                                                                                                                                                                                    | Padrão para NULL                                                                                                                                                                             | Padrão para NULL                                                                                                                                                                               |
| **Como os usuários podem alterar** | Opções regionais e de idioma<br/> (somente administradores)<br/>                                                                                                                                          | Opções regionais (item do painel de controle)<br/> **Windows XP:** Opções regionais e de idioma<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Padrão**              | **Windows Vista e posterior:** Idioma da versão localizada, seguido por qualquer fallback.                                                                                                                             | **Antes do Windows Vista:** Idioma da versão localizada.<br/> **Windows Vista e posterior:** Idioma da versão localizada, seguido por qualquer fallback.<br/>                     | Lista nula                                                                                                                                                                                     |
| **Função**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Processar idiomas de interface do usuário preferenciais                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Finalidade**              | **Windows 7 e posterior:** Determine os idiomas preferenciais para um processo de aplicativo. Para obter mais informações, consulte [User Interface Language Management](user-interface-language-management.md). |
| **Primeiro conjunto**            | Padrão para NULL                                                                                                                                                                                |
| **Como os usuários podem alterar** | Opções regionais e de idioma (somente administradores)                                                                                                                                            |
| **Padrão**              | **Windows 7 e posterior:** Idioma da versão localizada, seguido por qualquer fallback.                                                                                                             |
| **Função**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Página de Código

A incapacidade das páginas de código de ponto de 256 códigos para dar suporte à combinação de scripts em um único texto foi uma das principais razões para o aumento do Unicode. As páginas de código permanecem importantes para escrever código de console, para manter aplicativos herdados ou executar em versões mais antigas do Windows e para fazer a interface com alguns softwares não Microsoft que não são habilitados para Unicode.

## <a name="input-language"></a>Idioma de entrada

O idioma de entrada é representado por uma variável de dados por processo que descreve uma linguagem (por exemplo, grego) e um método de entrada (por exemplo, o teclado). Várias linguagens de entrada podem ser instaladas e o usuário pode alternar entre elas.

Para definir e recuperar o valor do idioma de entrada, o aplicativo chama [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) e [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout), respectivamente. Os usuários podem adicionar e remover idiomas de entrada por meio da guia **idiomas** na parte de opções regionais e de idiomas do painel de controle.

O idioma de entrada padrão é o idioma localizado do sistema operacional, e é a configuração que está ativa quando um novo aplicativo é iniciado (ou quando uma nova janela é aberta para alguns aplicativos). Alternar para um idioma de entrada diferente é feito por aplicativo. Em outras palavras, dois idiomas de entrada diferentes podem ser usados em dois aplicativos diferentes. Por exemplo, um usuário pode digitar alemão usando o layout de teclado internacional Estados Unidos, inglês usando entrada de voz (com software não Microsoft) e espanhol usando um IME em três aplicativos diferentes.

## <a name="language-for-non-unicode-programs"></a>Idioma para programas não Unicode

O idioma para programas não-Unicode (anteriormente chamados de "localidade do sistema") determina a página de código usada no sistema operacional por padrão. A configuração idioma para programas não Unicode afeta apenas aplicativos não-Unicode, ou seja, aplicativos ANSI. Definir o idioma instrui o Windows a emular um sistema operacional não baseado em Unicode, localizado nesse idioma. A alteração do idioma para programas não-Unicode instala os arquivos de fonte de bitmap necessários para dar suporte a aplicativos não Unicode no idioma especificado. Para permitir que o usuário selecione um idioma para programas não-Unicode, o grupo de idiomas apropriado deve ser instalado. Seu aplicativo precisa do suporte de script para selecionar um idioma para programas não-Unicode. O idioma para programas não-Unicode é uma configuração por sistema e requer a implementação de uma reinicialização.

Às vezes, não há nenhuma diferença perceptível entre dois idiomas para programas não-Unicode. Por exemplo, esse é o caso das localidades alemão (neutro) e alemão (Áustria). Em geral, as configurações de um grupo de idiomas são muito semelhantes e diferem apenas na página de código OEM ou MAC.

Um aplicativo ANSI deve verificar a configuração do idioma para programas não Unicode durante a instalação. Ele usa [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) ou [**GetOEMCP**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) para recuperar o valor. Nenhuma função tem suporte para definir o idioma para programas não-Unicode. No entanto, os usuários podem alterá-lo usando a guia **avançado** na parte de opções regionais e de idiomas do painel de controle. A seguir estão alguns exemplos de linguagem para configurações de programas não Unicode:

1.  Um usuário alemão que deseja executar um aplicativo em Japonês que foi projetado para o Windows 95 em Japonês deve selecionar o japonês como idioma para programas não-Unicode. Após essa seleção, os aplicativos em alemão não Unicode têm problemas. Por exemplo, os tremos de alemão (̈) não são exibidos corretamente.
2.  Um usuário em alemão que deseja digitar texto em Japonês em um aplicativo não Unicode em alemão deve selecionar japonês como idioma para programas não-Unicode. Como no primeiro exemplo, isso causa problemas na inserção de texto em alemão em aplicativos não-Unicode.
3.  Um usuário árabe que deseja digitar em árabe, francês e inglês em um aplicativo arábico não Unicode deve selecionar o árabe como um idioma para programas não-Unicode, pois a página de código ANSI árabe contém a maioria dos caracteres franceses e todos os caracteres em inglês.

## <a name="language-group"></a>Grupo de idiomas

O grupo de idiomas controla o idioma para programas, padrões e formatos não-Unicode, idiomas de entrada e idiomas de interface do usuário que podem ser selecionados. Para cada versão localizada, o grupo de idiomas especificado é o padrão e não pode ser removido. Por exemplo, o Windows instala o grupo de idiomas da Europa Ocidental e Estados Unidos por padrão. Portanto, se a versão em inglês do Windows estiver instalada em um país/região que não esteja em inglês, o usuário normalmente instalará outro grupo de idiomas.

Ao adicionar um grupo de idiomas, o Windows copia (mas não ativa) os arquivos de teclado necessários, os IMEs (Input Method Editors), os arquivos de fonte TrueType, os arquivos de fonte de bitmap e os arquivos. NLS (suporte ao idioma nacional). A adição de um grupo de idiomas também adiciona valores de registro para vinculação de fontes e instala mecanismos de script para linguagens de script complexas (árabe, Hebraico, Índico e tailandês).

Além do grupo de idiomas da Europa Ocidental e Estados Unidos, há 16 outros grupos de idiomas:



<table>
<tbody>
<tr class="odd">
<td><dl> Árabe<br />
Armênia<br />
Báltico<br />
Europa Central<br />
Cirílico<br />
Georgiano<br />
Grego<br />
Hebraico<br />
</dl></td>
<td><dl> Índia<br />
Japonês<br />
Coreano<br />
Chinês simplificado<br />
Chinês tradicional<br />
Tailandês<br />
Turco<br />
Vietnamita<br />
</dl></td>
</tr>
</tbody>
</table>



 

Qualquer número e combinação de grupos de idiomas pode ser instalado em qualquer sistema operacional. Por exemplo, um usuário espanhol pode instalar o grupo de idiomas cirílico para trabalhar em textos em Russo. Nesse caso, um aplicativo de processamento de texto precisa também oferecer suporte ao grupo de idiomas cirílico.

> [!Note]  
> A adição do grupo de idiomas apropriado não permite que um aplicativo aceite texto automaticamente. O teste é recomendado. Por exemplo, aplicativos não-Unicode podem exigir que o idioma para programas não-Unicode seja alterado.

 

## <a name="location"></a>Local

**Windows XP:** Um local é um identificador geográfico. Ele é representado por uma variável de dados por usuário que define o país/região onde o usuário reside.

Para definir o valor, o aplicativo chama [**SetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid). Para recuperar o valor, o aplicativo chama [**GetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid).

## <a name="standards-and-formats"></a>Padrões e formatos

Padrões e formatos (anteriormente "localidade do usuário") é uma variável por usuário que determina a ordem de classificação padrão e as configurações padrão para formatar datas, horas, moeda e números. A variável é apresentada como uma linguagem (às vezes em combinação com um país/região), mas não é uma linguagem em si. Por exemplo, definir a variável de padrões e formatos como Hebraico indica que o usuário deseja usar as convenções de formatação de Hebraico, não necessariamente a linguagem Hebraico. Além disso, a variável de padrões e formatos determina a cadeia de caracteres usada para os nomes de dias e meses. Por exemplo, se um usuário exibir "25 de novembro de 1998", a cadeia de caracteres "novembro" poderá mudar com base na variável de padrões e formatos. Alterar a variável adiciona automaticamente uma localidade de entrada com as configurações padrão para o idioma.

Para obter a configuração de variável de padrões e formatos, o aplicativo chama [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) ou [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename). Nenhuma função NLS está disponível para definir a variável. No entanto, os usuários podem alterá-lo por meio da guia **Opções de região** na parte de opções regionais e de idioma do painel de controle.

Um aplicativo normalmente deve usar as configurações de variável de padrões e formatos para exibir dados. No entanto, um aplicativo que usa uma localidade fixa para exibir dados deve passar um identificador de localidade específico em vez de usar o padrão de usuário de localidade \_ \_ .

## <a name="thread-locale"></a>Localidade do thread

A localidade do thread é representada por uma variável de dados de localidade por thread que determina a formatação de datas, horas, moedas e números grandes para o thread. O padrão é o valor para a localidade selecionada no momento para padrões e formatos. Para definir a localidade do thread, o aplicativo chama [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale). Para recuperar a localidade do thread, o aplicativo chama [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

Na maioria dos casos, a localidade do thread não deve ser substituída. Normalmente, ele só deve ser usado para sincronizar a localidade de thread de um aplicativo de servidor com a variável de padrões e formatos de um computador cliente. Por exemplo, um aplicativo financeiro de comércio de ações para a troca de ações de Nova York, que é usado em bancos em todo o mundo, tem que exibir a hora, a data e os preços de ações nos formatos de Estados Unidos. Esse aplicativo usa [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para definir a localidade do thread como inglês (Estados Unidos), em seguida, usa as funções NLS para formatar datas, horas e preços de ações.

A alteração da localidade do thread não afeta todas as funções de API. Portanto, nem sempre é uma maneira confiável de substituir a variável de padrões e formatos. Em vez disso, os aplicativos que controlam padrões e formatos devem usar uma localidade fixa para exibir dados, passando um identificador de localidade específico em vez de usar o padrão de usuário de localidade \_ \_ .

## <a name="nls-example"></a>Exemplo de NLS

O exemplo a seguir mostra a interatividade entre padrões e formatos, a linguagem para programas não Unicode, local e idioma de interface do usuário.

Um usuário que é nativo do Chile, mas está vivendo no Estados Unidos tem um computador com o Windows XP em inglês. O usuário define o local para Estados Unidos usar um provedor de serviços de Internet (ISP) para obter o clima da Estados Unidos. No entanto, a variável de padrões e formatos é definida como espanhol (Chile) para que as informações sejam formatadas de acordo com os padrões de chilena. Além disso, o usuário usa um processador de texto coreano, que é um aplicativo ANSI, para que o idioma de programas não-Unicode seja definido como coreano (Coreia). Para usar o aplicativo, o usuário tem um teclado em inglês e também instala um IME coreano para dar suporte a um segundo idioma de entrada. O colaborador do usuário, que compartilha o computador, mas não se sente confortável com o inglês, pode definir o idioma da interface do usuário para espanhol (Espanha) ao usar o computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> </dl>

 

 
