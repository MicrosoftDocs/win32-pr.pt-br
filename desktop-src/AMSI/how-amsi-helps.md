---
title: Como o AMSI ajuda você a se defender contra malware
description: Como desenvolvedor de aplicativos, você pode participar ativamente da defesa contra malware. Especificamente, você pode ajudar a proteger seus clientes contra malwares baseados em script dinâmicos e de caminhos não tradicionais do cyberattack.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635118"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Como a interface de verificação antimalware (AMSI) ajuda você a se defender contra malware

Para obter uma introdução à AMSI (interface de verificação antimalware) do Windows, consulte [interface de verificação antimalware (AMSI)](antimalware-scan-interface-portal.md).

Como desenvolvedor de aplicativos, você pode participar ativamente da defesa contra malware. Especificamente, você pode ajudar a proteger seus clientes contra malwares baseados em script dinâmicos e de caminhos não tradicionais do cyberattack.

Por meio de um exemplo, digamos que seu aplicativo seja programável por script: ele aceita um script arbitrário e o executa por meio de um mecanismo de script. No ponto em que um script está pronto para ser fornecido ao mecanismo de script, seu aplicativo pode chamar as APIs AMSI do Windows para solicitar uma verificação do conteúdo. Dessa forma, você pode determinar com segurança se o script é mal-intencionado antes de decidir continuar e executá-lo.

Isso é verdadeiro mesmo que o script tenha sido gerado em tempo de execução. Script (mal-intencionado ou de outra forma) pode passar por várias passagens de desofuscação. Mas, em última instância, você precisa fornecer o mecanismo de script com código simples e não ofuscado. E esse é o ponto no qual você invoca as APIs AMSI.

Aqui está uma ilustração da arquitetura AMSI, em que seu próprio aplicativo é representado por uma das caixas "outros aplicativos".

![a arquitetura AMSI](images/AMSI7Archi.jpg)

A interface AMSI do Windows está aberta. O que significa que qualquer aplicativo pode chamá-lo; e qualquer mecanismo Antimalware registrado pode processar o conteúdo enviado a ele.

Também não precisamos limitar a discussão a mecanismos de script. Talvez seu aplicativo seja um aplicativo de comunicação e examine mensagens instantâneas em busca de vírus antes de mostrar a eles os clientes. Ou talvez seu software seja um jogo que valida os plug-ins antes de instalá-los. Há muitas oportunidades e cenários para usar o AMSI.

## <a name="amsi-in-action"></a>AMSI em ação

Vamos dar uma olhada em AMSI em ação. Neste exemplo, o Windows Defender é o aplicativo que está chamando APIs AMSI. Mas você pode chamar as mesmas APIs de dentro de seu próprio aplicativo.

Aqui está um exemplo de um script que usa a técnica de codificação XOR para ocultar sua intenção (se essa intenção é benigna ou não). Para esta ilustração, podemos imaginar que esse script foi baixado da Internet.

![script de exemplo codificado em base64](images/AMSI8.png)

Para tornar as coisas mais interessantes, podemos inserir esse script manualmente na linha de comando para que não haja nenhum arquivo real a ser monitorado. Isso espelha o que é conhecido como "ameaça de arquivo". Não é tão simples quanto verificar arquivos em disco. A ameaça pode ser um backdoor que reside apenas na memória de um computador.

A seguir, vemos o resultado da execução do script no Windows PowerShell. Você verá que o Windows Defender é capaz de detectar o exemplo de teste AMSI nesse cenário complicado, simplesmente usando a assinatura de exemplo de teste AMSI padrão.

![Windows Defender detectando o exemplo de teste do AMSI](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>Integração do AMSI com JavaScript/VBA

O fluxo de trabalho ilustrado abaixo descreve o fluxo de ponta a ponta de outro exemplo, no qual Demonstramos a integração de AMSI com a execução de macro dentro de Microsoft Office.

![Integração do AMSI com JavaScript/VBA](images/integ-js-vba.png)

- O usuário recebe um documento que contém uma macro (mal-intencionado), que evita exames de software antivírus estáticos empregando técnicas como ofuscação, arquivos protegidos por senha ou outros.
- O usuário abre o documento que contém a macro (mal-intencionado). Se o documento for aberto no modo de exibição protegido, o usuário clica em **Habilitar edição** para sair da exibição protegida.
- O usuário clica em **habilitar macros** para permitir a execução de macros.
- À medida que a macro é executada, o tempo de execução do VBA usa um buffer circular para registrar \[ 1 \] dados e parâmetros relacionados a chamadas para APIs do Win32, com e VBA.
- Quando APIs específicas do Win32 ou COM que são consideradas alto risco (também conhecidos como *gatilhos*) \[ 2 \] são observadas, a execução da macro é interrompida e o conteúdo do buffer circular é passado para AMSI.
- O provedor de serviços Antimalware AMSI registrado responde com um veredicto para indicar se o comportamento da macro é mal-intencionado ou não.
- Se o comportamento for não-mal-intencionado, a execução da macro continuará.
- Caso contrário, se o comportamento for mal-intencionado, Microsoft Office fechar a sessão em resposta ao alerta \[ 3 \] , e o AV poderá colocar o arquivo em quarentena.

## <a name="what-does-this-mean-for-you"></a>O que isso significa para você?

Para usuários do Windows, qualquer software mal-intencionado que usa técnicas de ofuscação e evasão nos hosts de script internos do Windows 10 é inspecionado automaticamente em um nível muito mais profundo do que nunca, fornecendo níveis adicionais de proteção.

Para você como desenvolvedor de aplicativos, considere fazer com que seu aplicativo chame a interface AMSI do Windows se você quiser se beneficiar (e proteger seus clientes com) a verificação extra e a análise de conteúdo potencialmente mal-intencionado.

Como um fornecedor de software antivírus, você pode considerar a implementação de suporte para a interface AMSI. Quando você fizer isso, seu mecanismo terá uma percepção muito mais profunda dos dados que os aplicativos (incluindo hosts de script interno do Windows 10) consideram potencialmente mal-intencionados.

## <a name="more-background-info-about-fileless-threats"></a>Mais informações básicas sobre ameaças de arquivo

Você pode estar curioso para obter mais informações sobre os tipos de ameaças de arquivo que o Windows AMSI foi projetado para ajudá-lo a se defender. Nesta seção, vamos dar uma olhada no jogo tradicional de gato e mouse que é executado no ecossistema de malware.

Usaremos o PowerShell como exemplo. Mas você pode aproveitar as mesmas técnicas e processos que demonstraremos com qualquer linguagem dinâmica &mdash; VBScript, Perl, Python, Ruby e muito mais.

Aqui está um exemplo de um script do PowerShell mal-intencionado.

![um exemplo de um script do PowerShell mal-intencionado](images/AMSI1.png)

Embora esse script simplesmente grave uma mensagem na tela, o malware normalmente é mais perigoso. Mas você pode facilmente escrever uma assinatura para detectar esta. Por exemplo, a assinatura pode pesquisar a cadeia de caracteres "Write-Host ' pWnd! '" em qualquer arquivo que o usuário abrir. Ótimo: detectamos nosso primeiro malware!

Depois de ser detectado pela nossa primeira assinatura, no entanto, os autores de malware responderão. Eles respondem Criando scripts dinâmicos, como este exemplo.

![um exemplo de um script dinâmico](images/AMSI2.png)

Nesse cenário, os autores de malware criam uma cadeia de caracteres que representa o script do PowerShell a ser executado. Mas eles usam uma técnica de concatenação de cadeia de caracteres simples para interromper nossa assinatura anterior. Se você já tiver exibido a origem de uma página da Web AD-carregados, verá muitas instâncias dessa técnica sendo usadas para evitar o software de bloqueio de anúncios.

Por fim, o autor de malware passa essa cadeia de caracteres concatenada para o `Invoke-Expression` &mdash; mecanismo do PowerShell do cmdlet para avaliar os scripts que são compostos ou criados no tempo de execução.

Em resposta, o software antimalware começa a fazer a emulação de linguagem básica. Por exemplo, se observarmos que duas cadeias de caracteres estão sendo concatenadas, emularemos a concatenação dessas duas cadeias de caracteres e, em seguida, executaremos nossas assinaturas no resultado. Infelizmente, essa é uma abordagem bastante frágil, porque as linguagens tendem a ter várias maneiras de representar e concatenar cadeias de caracteres.

Então, depois de ser capturado por essa assinatura, os autores de malware mudarão para algo mais complicado, &mdash; por exemplo, codificando o conteúdo do script em base64, como neste exemplo a seguir.

![um exemplo de conteúdo de script em base64](images/AMSI3.png)

Sendo versátil, a maioria dos mecanismos antimalware implementam a emulação de decodificação de Base64 também. Portanto, como também implementamos a emulação de decodificação de Base64, estamos à frente por um tempo.

Em resposta, os autores de malware mudam para ofuscação de algoritmo &mdash; , como um mecanismo simples de codificação XOR nos scripts que eles executam.

![um exemplo de um script de ofuscação de algoritmo](images/AMSI4.png)

Neste ponto, geralmente, nos deparamos com o que os mecanismos antivírus irão emular ou detectar, portanto, não detectaremos necessariamente o que esse script está fazendo. No entanto, podemos começar a escrever assinaturas com base nas técnicas de ofuscação e codificação. Na verdade, é isso que as contas para a grande maioria das assinaturas para malware baseado em script.

Mas e se o ofuscador for tão trivial que parece muitos scripts bem comparados? Uma assinatura para ela geraria um número inaceitável de falsos positivos. Aqui está um exemplo de script de *estágio* que é benigno demais para detectar por conta própria.

![um exemplo de script de teste que é benigno demais para detectar por conta própria](images/AMSI5.png)

Nesse exemplo, estamos baixando uma página da Web e invocando algum conteúdo dela. Aqui está o equivalente em Visual Basic Script.

![o equivalente em Visual Basic script](images/AMSI6.png)

O que torna as coisas piores em ambos os exemplos é que o mecanismo antivírus inspeciona os arquivos que estão sendo abertos pelo usuário. Se o conteúdo mal-intencionado residir apenas na memória, o ataque pode potencialmente não ser detectado.

Esta seção mostrou as limitações de detecção usando assinaturas tradicionais. Mas, embora um script mal-intencionado possa passar por várias passagens de desofuscação, ele, por fim, precisa fornecer o mecanismo de script com código simples e sem ofuscação. E nesse ponto &mdash; , conforme descrito na primeira seção acima, os &mdash; hosts de script internos do Windows 10 chamam as APIs AMSI para solicitar uma verificação desse conteúdo desprotegido. E seu aplicativo pode fazer a mesma coisa.

## <a name="related-resources"></a>Recursos relacionados

* [Ameaças sem arquivo](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI: parte do vela em macros mal-intencionadas](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Fora de visão, mas não invisível: disparando malware sem arquivo com monitoramento de comportamento, AMSI e AV de próxima geração](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
