---
title: Melhores práticas de segurança no desenvolvimento de jogos
description: Este artigo aborda as práticas recomendadas para uso no desenvolvimento de jogos.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba4f02d5e1a2e3da2e50feedd89f085a0c063be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823856"
---
# <a name="best-security-practices-in-game-development"></a>Melhores práticas de segurança no desenvolvimento de jogos

Este artigo aborda as práticas recomendadas para uso no desenvolvimento de jogos.

-   [Introdução](#introduction)
-   [Exemplos de código não seguro](#examples-of-insecure-code)
-   [Maneiras de melhorar a segurança](#ways-to-improve-security)
-   [Resumo](#summary)

## <a name="introduction"></a>Introdução

Um número cada vez maior de pessoas desempenham jogos e jogos online com conteúdo feito pelo usuário. Isso, combinado com o aumento da segurança do sistema operacional Microsoft Windows, significa que os jogos são um alvo crescente e mais tentador para os invasores explorarem. Os desenvolvedores de jogos devem tomar uma ênfase forte em garantir que os jogos que eles lançam não estejam criando novos buracos de segurança para que os invasores possam explorar. Os desenvolvedores de jogos têm uma responsabilidade e um interesse para ajudar a impedir que os computadores dos clientes sejam invadidos por dados mal-intencionados da rede, modificações do usuário ou adulterações. Se uma vulnerabilidade for explorada, isso poderá resultar na perda de clientes e/ou dinheiro. Este artigo descreve e explica alguns métodos e ferramentas comuns para aumentar a segurança do código sem o tempo de desenvolvimento excessivo.

Os três erros mais comuns feitos por uma equipe de desenvolvimento ao lançar um produto são:

-   Exigindo privilégios administrativos. Os jogos não devem exigir privilégios administrativos. Para obter mais detalhes, consulte [controle de conta de usuário para desenvolvedores de jogos](./user-account-control-for-game-developers.md).
-   Não usar proteção automatizada. Os desenvolvedores geralmente não estão usando **/GS**, **/SAFESEH** ou **/NX**. Usar esses sinalizadores de compilação/link pode identificar ou eliminar muitos buracos de segurança básicos sem aumentar significativamente a carga de trabalho. Esses sinalizadores serão discutidos posteriormente neste artigo.
-   Usando APIs proibidas. Há muitas APIs (**strcpy**, **strncpy** e assim por diante) que estão sujeitas a erros do programador e geram brechas de segurança com facilidade. Os desenvolvedores devem substituir essas APIs pelas versões seguras. O Visual Studio 2005 vem com uma ferramenta para analisar arquivos binários que podem verificar automaticamente os arquivos de objeto em busca de referências a APIs não seguras. Para obter mais informações sobre o que fazer com as informações geradas com essa ferramenta, consulte [ataques de repelir em seu código com as bibliotecas C e C++ seguras do Visual Studio 2005](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) por Martyn Lovell. Além disso, você pode obter o arquivo de cabeçalho [. h banido](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) que pode ajudá-lo a remover funções banidas do código.

Cada um dos erros listados não é apenas comum, mas é facilmente corrigível sem alterações significativas na carga de trabalho de desenvolvimento, padrões de codificação ou funcionalidade.

## <a name="examples-of-insecure-code"></a>Exemplos de código não seguro

Veja a seguir um exemplo simples de tudo o que é necessário para permitir que um invasor execute um ataque de saturação de buffer:


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



Na superfície, esse código parece ok — ele chama uma função segura, afinal. Os dados da rede são copiados em um buffer que é de 256 bytes. A função **strncpy** se baseia na localização de um terminador nulo na cadeia de caracteres de origem ou é limitada pela contagem de buffer fornecida. O problema é que o tamanho do buffer está incorreto. Se os dados da rede não forem validados ou o tamanho do buffer estiver errado (como neste exemplo), um invasor poderá simplesmente fornecer um buffer grande para substituir os dados da pilha, depois que o buffer terminar, com todos os dados no pacote de rede. Isso permitiria que o invasor executasse código arbitrário substituindo o ponteiro de instrução e alterando o endereço de retorno. A lição mais básica deste exemplo é nunca confiar na entrada até que ela tenha sido verificada.

Mesmo que os dados não venham da rede inicialmente, ainda há um risco potencial. O desenvolvimento de jogos modernos requer muitas pessoas criando, desenvolvendo e testando a mesma base de código. Não há como saber como a função será chamada no futuro. Sempre perguntar de onde vêm os dados e o que um invasor poderia controlar? Embora os ataques baseados em rede sejam os mais comuns, eles não são os únicos métodos de criação de brechas de segurança. Um invasor pode criar um mod ou editar um arquivo salvo de uma maneira que abre uma brecha de segurança? E quanto aos arquivos de imagem e som fornecidos pelo usuário? As versões mal-intencionadas desses arquivos podem ser publicadas na Internet e criar riscos de segurança perigosos para seus clientes.

Como uma observação adicional, Use strsafe. h ou CRT seguro em vez de **strncpy** para corrigir o exemplo. O CRT seguro é uma revisão de segurança completa do tempo de execução do C e vem com parte do Visual Studio 2005. Mais informações sobre o CRT seguro podem ser encontradas em [aprimoramentos de segurança no CRT](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) por Michael Howard.

## <a name="ways-to-improve-security"></a>Maneiras de melhorar a segurança

Há várias maneiras de melhorar a segurança no ciclo de desenvolvimento. Aqui estão algumas das melhores maneiras:

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>Lendo sobre segurança
</dt> <dd>

O livro, *escrevendo código seguro, segunda edição* de Michael Howard e David LeBlanc, fornece uma explicação detalhada e clara de estratégias e métodos de impedir ataques e mitigar explorações. Começando com métodos de criação de segurança em uma versão para técnicas de proteção de aplicativos de rede, o livro abrange todos os aspectos que um desenvolvedor de jogos precisa para ajudar a se proteger, seus produtos e seus clientes contra invasores. O livro pode ser usado para incutir uma cultura de segurança em um estúdio de desenvolvimento. Não imagine apenas a segurança de código como o problema de um desenvolvedor ou o problema de um testador. Pense na segurança como algo que a equipe inteira — do gerente de programa ao designer do desenvolvedor a ser testador — deve estar pensando quando trabalha em um projeto. Quanto mais olhos fizerem parte do processo de revisão, maior será a chance de capturar uma brecha de segurança antes do lançamento.

*Escrever código seguro, a segunda edição,* pode ser encontrado no [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) e informações de segurança mais gerais podem ser encontradas em [fending de ataques futuros, reduzindo a superfície de ataque](/previous-versions/ms972812(v=msdn.10)) de Michael Howard.

Michael Howard, David LeBlanc e John Viega escreveu outro livro sobre o assunto que abrange todos os sistemas operacionais comuns e linguagens de programação intitulados, *19 Deadly Sins da segurança de software*.

Apresentações de segurança focadas em jogos podem ser encontradas na página de download de [apresentações para desenvolvedores do Microsoft XNA](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Análise de modelagem de ameaças
</dt> <dd>

Uma análise de modelagem de ameaças é uma boa maneira de avaliar a segurança do sistema, não em uma linguagem específica ou usando uma ferramenta, mas em um método amplo de ponta a ponta que pode ser feito em algumas reuniões. Quando implementado corretamente, um modelo de thread pode identificar todos os pontos fortes e fracos de um sistema, sem adicionar carga de trabalho significativa ou tempo de reunião ao projeto. O método de modelagem de ameaças também enfatiza a ideia de avaliar a segurança do sistema antes e durante o processo de desenvolvimento para ajudar a garantir que uma avaliação abrangente esteja sendo feita enquanto se concentra nos recursos mais arriscados. Pode ser pensado como um criador de perfil para segurança. Sem se basear em uma linguagem específica ou depender de uma ferramenta específica, a modelagem de risco pode ser usada em qualquer estúdio de desenvolvimento que trabalhe em qualquer projeto em qualquer gênero. A modelagem de ameaças também é um método excelente de reforçar a ideia de que a segurança é a responsabilidade de todos, e não o problema de outra pessoa.

Quando a modelagem de ameaças, preste atenção especial a:

-   Fontes de dados UDP
-   Fontes de dados que não exigem autenticação
-   Fontes de dados que são frequentemente e normalmente investigadas como parte da coleta de informações em larga escala
-   Qualquer capacidade de um cliente de enviar dados diretamente para outros clientes

Essas são as áreas que têm bom potencial para pontos fracos de segurança.

Mais sobre a modelagem de ameaças pode ser encontrada em [modelagem de ameaças](https://technet.microsoft.com/security/) no MSDN Security Development Center e no livro [Threat Modeling](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) by Frank Swiderski e Window Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Prevenção de execução de dados (/NX)
</dt> <dd>

Uma ferramenta recente na mitigação de várias explorações é A DEP (prevenção de execução de dados). Se você incluir o switch **/NX** no comando Build, o Visual Studio marcará páginas de memória com sinalizadores que denotam se o código tem o direito de executar ou não. Qualquer programa que tente executar em uma página de memória não sinalizada com a permissão executar causará um encerramento Forcible do programa. A prevenção é imposta no nível do processador e afetará os desenvolvedores que usam código de modificação automática ou compiladores de linguagem JIT nativos. Atualmente, somente os processadores Athlon64 e Opteron da AMD e os processadores Pentium 4 da Intel e mais recentes suportam a prevenção de execução, mas é esperado que todos os processadores de 32 bits e 64 bits ofereçam suporte à prevenção de execução no futuro. (Um esquema de proteção de cópia usado por um desenvolvedor pode ser afetado pela prevenção de execução, mas a Microsoft tem trabalhado com fornecedores de proteção de cópia para minimizar o impacto.) É uma boa prática usar o DEP.

Para obter mais detalhes sobre o DEP, consulte [prevenção de execução de dados](../memory/data-execution-prevention.md).

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>Verificação de segurança de buffer (/GS) e imagem tem manipuladores de exceção seguros (/SAFESEH)
</dt> <dd>

A *verificação de segurança do buffer*, especificada pelo sinalizador do compilador **/GS**, e a *imagem tem manipuladores de exceção seguros*, especificados pelo sinalizador do vinculador **/SAFESEH** (implementado pela primeira vez no Visual Studio .NET 2003), pode tornar o trabalho do desenvolvedor de proteger o código um pouco mais fácil.

O uso do sinalizador **/GS** faz com que o compilador Construa uma verificação de algumas formas de saturações de buffer baseadas em pilha que poderiam ser exploradas para substituir o endereço de retorno de uma função. O uso do **/GS** não detectará todas as possíveis saturações de buffer e não deve ser considerado uma boa tecnologia de defesa aprofundada.

O uso do sinalizador **/SAFESEH** instruirá o vinculador a gerar apenas um executável ou dll se ele também puder gerar uma tabela dos manipuladores de exceção segura do executável ou da dll. O SafeSEH (tratamento de exceção estruturada) elimina a manipulação de exceções como um destino de ataques de saturação de buffer, garantindo que, antes que uma exceção seja expedida, o manipulador de exceção seja registrado na tabela de funções localizada no arquivo de imagem. Esses benefícios de proteção estão habilitados com o Windows XP SP2, o Windows Server 2003, o Windows Vista e o Windows 7. Além disso, para que o **/SAFESEH** funcione corretamente, ele deve ser usado em um método tudo ou nada. Todas as bibliotecas que contêm código associado a um executável ou DLL devem ser compiladas com **/SAFESEH** ou a tabela não será gerada.

Mais informações sobre a [verificação de segurança do buffer](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/GS**) e a [imagem têm manipuladores de exceção seguros](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/SAFESEH**) podem ser encontradas no msdn.

Consulte também informações sobre o [sinalizador **/SDL**](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) do Microsoft Visual Studio 2012 e os aprimoramentos do Visual Studio 2012 [para o sinalizador **/GS**](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/).

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

O PREfast é uma ferramenta gratuita oferecida pela Microsoft que analisa os caminhos de execução em C ou C++ compilado para ajudar a encontrar bugs em tempo de execução. O PREfast Opera trabalhando com todos os caminhos de execução em todas as funções e avaliando cada caminho quanto a problemas. Usado originalmente para desenvolver drivers e outros códigos de kernel, essa ferramenta pode ajudar os desenvolvedores de jogos a economizar tempo, eliminando alguns bugs que são difíceis de encontrar ou ignorados pelo compilador. Usar o PREfast é uma maneira excelente de reduzir a carga de trabalho e concentrar os esforços da equipe de desenvolvimento e da equipe de teste. O PREfast está disponível no Visual Studio Team Suite e no Visual Studio Team Edition for Software Developers como análise de código, habilitado pela opção do compilador **/Analyze**. (Essa opção também está disponível na versão gratuita do compilador que acompanha o kit de desenvolvimento de software do Windows.)

> [!Note]  
> O Visual Studio 2012 dá suporte a **/Analyze** em todas as edições. Para obter mais informações sobre a disponibilidade da análise de código em todas as edições do Visual Studio, consulte [novidades na análise de código](/archive/blogs/codeanalysis/?m=20123).

 

Com o uso da anotação de cabeçalho (particularmente para argumentos de ponteiro de buffer), o PREfast pode expor problemas adicionais, como erros de substituição de memória, uma fonte comum de falhas e vulnerabilidades de segurança em potencial. Isso é feito usando a linguagem de anotação padrão (SAL), que é uma forma de marcação para protótipos de função C/C++ que fornecem informações adicionais sobre a semântica de argumento de ponteiro esperada e correlação com parâmetros de comprimento, tamanhos de buffer declarados, etc. Todos os cabeçalhos dos sistemas operacionais Windows são anotados e a adição de marca SAL em cabeçalhos de API pública em suas próprias bibliotecas permite a realização de verificações mais detalhadas e agressivas em seu código de cliente para tais APIs. Para obter uma introdução ao SAL e a links para mais informações, consulte a entrada de blog de Michael Howard, "[uma breve introdução à linguagem de anotação padrão (sal)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)".

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Application Verifier do Windows
</dt> <dd>

O Windows Application Verifier, ou AppVerifier, pode ajudar os testadores fornecendo várias funções em uma ferramenta. O AppVerifier é uma ferramenta desenvolvida para tornar mais testados os erros comuns de programação. O AppVerifier pode verificar os parâmetros passados para chamadas à API, injetar entrada errada para verificar a capacidade de tratamento de erros e registrar em log as alterações no registro e no sistema de arquivos. O AppVerifier também pode detectar saturações de buffer no heap, verificar se uma ACL (lista de controle de acesso) foi definida corretamente e impor o uso seguro de APIs de soquete. Embora não seja exaustiva, o AppVerifier pode ser uma ferramenta na caixa de ferramentas do testador para ajudar um produto do Development Studio a lançar uma qualidade.

Para obter mais informações sobre Application Verifier, consulte [Application Verifier](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) e [usando Application Verifier em seu ciclo de vida de desenvolvimento de software](/previous-versions/aa480483(v=msdn.10)) no msdn.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Teste de fuzzing
</dt> <dd>

O *teste difuso* é um método semiautomatizado de testes que pode aprimorar as metodologias de teste atuais. A ideia central por trás do teste de fuzzing é fazer uma avaliação completa de todas as entradas inserindo dados aleatórios para ver quais são as interrupções; Isso inclui todos os dados de rede, mods e jogos salvos, etc. O teste difuso é razoavelmente fácil de fazer. Basta alterar arquivos bem formados ou dados de rede inserindo bytes aleatórios, invertendo bytes adjacentes ou negando valores numéricos. 0xFF, 0xFFFF, 0xFFFFFFFF, 0x00, 0x0000, 0x00000000 e 0x80000000 são valores que são bons na exposição de brechas de segurança durante o teste de difusão. Você pode observar as combinações de interação resultantes usando o AppVerifier. Embora a difusão não seja exaustiva, é fácil implementar e automatizar, e pode detectar bugs mais enganosos e imprevisíveis.

Para obter mais informações sobre testes de fuzzing, consulte as *etapas práticas* de apresentação do [Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) em segurança do jogo.

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Assinatura Authenticode
</dt> <dd>

O Authenticode é um método para garantir que arquivos executáveis, arquivos DLL e pacotes do Windows Installer (arquivos. msi) que o usuário recebe sejam inalterados do que um desenvolvedor lançou. Usando uma combinação de princípios de criptografia, entidades confiáveis e padrões do setor, o Authenticode verifica a integridade do conteúdo executável. A Microsoft fornece uma API criptográfica, CryptoAPI, que pode ser usada para detectar automaticamente a adulteração de código assinado. Se um vazamento de segurança ocorrer após uma versão, um certificado poderá ser revogado e todo o código assinado com esse certificado deixará de ser autenticado. Revogar um certificado revogará a validação de todos os títulos assinados com esse certificado. O Windows foi projetado para trabalhar com assinatura Authenticode e alertará um usuário de código não assinado, em situações específicas, que poderia expor o computador de um usuário a ataques.

O Authenticode não deve ser considerado um método de eliminação de problemas de segurança, mas um método de detecção de adulteração após um executável foi lançado. Um executável ou DLL que contém um problema de segurança explorável pode ser assinado e verificado usando o Authenticode, mas ele ainda apresentará o problema de segurança para o novo sistema. Somente depois que um produto ou atualização tiver sido verificado para ser seguro, caso o código seja assinado para garantir que os usuários tenham uma versão que não tenha sido adulterada.

Mesmo se o desenvolvedor sentir que não há nenhuma ameaça de suas versões sendo modificadas, outras tecnologias e serviços dependem do Authenticode. A assinatura de código é fácil de integrar e automatizar; Não há motivo para os desenvolvedores não terem suas versões assinadas.

Para obter mais informações sobre assinatura Authenticode, consulte [assinatura Authenticode para desenvolvedores de jogos](./authenticode-signing-for-game-developers.md).

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Minimizar privilégios
</dt> <dd>

Em geral, os processos devem ser executados com o conjunto mínimo de privilégios necessários para operar. No Windows Vista e no Windows 7, isso é feito usando o [controle de conta de usuário](./user-account-control-for-game-developers.md), permitindo que o jogo seja executado como um usuário padrão em vez de um administrador. Para o Windows XP, normalmente os jogos estão sempre em execução como administrador. Mesmo no Windows Vista e no Windows 7, às vezes é necessário elevar a direitos de administrador completo para algumas operações específicas.

Nos casos em que o processo está sendo executado com direitos administrativos completos, normalmente apenas alguns direitos além daqueles de um usuário padrão são realmente necessários. O acesso administrativo inclui muitos direitos que não são exigidos pelo código legítimo, mas que podem ser usados por um invasor, por meio de algum ponto fraco no processo. Exemplos de tais direitos incluem SE \_ apropriar-se \_ , se for, \_ debug, se \_ Create \_ token, se \_ ASSIGNPRIMARYTOKEN, se TCB, se \_ \_ Security, o \_ Load \_ Driver, se for \_ SYSTEMTIME, \_ backup, se o Restore, o \_ \_ desligamento se e a \_ auditoria se (consulte [constantes de privilégio](../secauthz/privilege-constants.md)).

Embora um processo não possa obter mais direitos depois de iniciado, ele pode facilmente fornecer direitos. Na inicialização, o processo pode usar imediatamente as APIs do Win32 para remover os direitos que ele não precisa.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>Utilizar os recursos de segurança do Windows
</dt> <dd>

O Windows Vista e o Windows 7 incluem vários recursos novos que aprimoram a segurança do código. O [controle de conta de usuário](./user-account-control-for-game-developers.md) é certamente o mais importante para entender e adotar, mas também há outros recursos. Além das tecnologias do Windows XP SP2, como o Firewall do Windows, a prevenção de execução de dados, a verificação de segurança do buffer e os manipuladores de exceção segura que também estão disponíveis no Windows Vista e no Windows 7, há três recursos de segurança mais recentes a serem considerados:

-   O recurso de randomização de layout de espaço de endereço de aceitação. Isso é habilitado por meio da vinculação com a opção **/DynamicBase** no visual Studio 2005 Service Pack 1 ou no visual Studio 2008. Isso faz com que o sistema torne aleatório as posições de muitas das principais DLLs do sistema em seu espaço de processo, tornando muito mais difícil escrever programas de ataque exploráveis que se propaguem amplamente pela Internet. Esse sinalizador de vinculador é ignorado pelo Windows XP e por versões anteriores do Windows.
-   A corrupção de heap pode levar a uma classe inteira de explorações de segurança, portanto, o sistema de memória do Windows Vista e do Windows 7 agora oferece suporte a um modo que encerra o processo se a corrupção de heap for detectada. Chamar [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) com **HeapEnableTermianteOnCorruption** aceitará esse comportamento. Essa chamada falha no Windows XP e na versão mais antiga do Windows.
-   Ao escrever serviços, eles podem ser configurados usando um novo recurso para especificar quais privilégios são realmente necessários, bem como para limitar o acesso de recursos a um SID específico. Isso é feito por meio de [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a), usando as \_ \_ \_ \_ informações de privilégios necessários de configuração de serviço e informações de SID do serviço de configuração de serviço \_ \_ \_ \_ .

</dd> </dl>

## <a name="summary"></a>Resumo

Desenvolver um jogo para o Marketplace atual e futuro é dispendioso e demorado. Lançar um jogo com problemas de segurança, por fim, custará mais dinheiro e tempo para corrigir corretamente. Portanto, é interessante que todos os desenvolvedores de jogos integrem ferramentas e técnicas para atenuar as explorações de segurança antes do lançamento.

As informações neste artigo são apenas uma introdução ao que um Development Studio pode fazer para ajudar a si mesmos e seus clientes. Mais informações sobre práticas de segurança e informações de segurança gerais podem ser encontradas no [Microsoft Security Developer Center](https://technet.microsoft.com/security/).

 

 