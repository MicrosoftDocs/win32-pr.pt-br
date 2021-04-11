---
description: Este tópico descreve como você pode trabalhar com IDNs (nomes de domínio internacionalizados) em seus aplicativos.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Tratando IDNs (nomes de domínio internacionalizados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170435"
---
# <a name="handling-internationalized-domain-names-idns"></a>Tratando IDNs (nomes de domínio internacionalizados)

Este tópico descreve como você pode trabalhar com IDNs (nomes de domínio internacionalizados) em seus aplicativos. Os IDNs são especificados pelo grupo de trabalho [de rede RFC 3490: Internacionalizando nomes de domínio em aplicativos (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). Antes desse padrão de rascunho, os IDNs eram limitados a caracteres latinos sem sinais diacríticos. O IDNA permite que IDNs inclua caracteres latinos com sinais diacríticos, juntamente com caracteres de scripts não latinos, como cirílico, árabe e chinês. O padrão também estabelece regras para mapear IDNs para nomes de domínio somente ASCII. Assim, problemas de IDNA podem ser tratados no lado do cliente, sem a necessidade de qualquer alteração de DNS (servidor de nome de domínio).

> [!Caution]  
> A RFC 3490 apresenta vários problemas de segurança relacionados ao uso de IDNs. Para obter mais informações, consulte a seção relacionada de [considerações de segurança: recursos internacionais](security-considerations--international-features.md).

 

> [!Note]  
> O IDNA atualmente é baseado em Unicode 3,2.

 

## <a name="nls-api-functions-for-handling-idns"></a>Funções da API NLS para manipulação de IDNs

O NLS inclui as seguintes funções de conversão que seu aplicativo pode usar para converter um IDN em representações diferentes. Para obter um exemplo do uso dessas funções, consulte [exemplo de conversão NLS: nome de domínio internacionalizado (IDN)](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Converte um IDN em Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Executa a parte NamePrep da conversão de um IDN em um nome ASCII. Essa função cria uma representação Unicode canônica de uma cadeia de caracteres.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Converte uma cadeia de caracteres Punycode em uma cadeia de caracteres UTF-16 normal.

O NLS também define várias funções de API que podem ser usadas para atenuar alguns dos riscos de segurança apresentados pela tecnologia IDN. No Windows Vista e posterior, as funções a seguir são usadas para verificar se os caracteres em um determinado IDN são desenhados inteiramente dos scripts associados a uma localidade ou localidades em particular. Para obter um exemplo do uso dessas funções, consulte [NLS: exemplo de mitigação do IDN (nome de domínio internacionalizado)](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Fornece uma lista de scripts usados em uma cadeia de caracteres específica.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Recuperar informações de localidade. Usar as funções com *LCTYPE* definido como [localidade \_ SSCRIPTS](locale-sscripts.md) fornece uma lista de scripts normalmente usados para uma localidade específica.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Compara listas de scripts. Para verificar em várias localidades, o aplicativo pode fazer várias chamadas para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) e [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

Para aplicativos executados no Windows XP e no Windows Server 2003, as funções [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md), [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)e [**DownlevelVerifyScripts**](downlevelverifyscripts.md) desempenham uma função semelhante às funções listadas acima em mitigar o risco de segurança. O download ["APIs de mitigação do IDN (Microsoft Internacionalizated Domain Name)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) está disponível no [centro de download do MSDN](https://www.microsoft.com/?ref=go).

## <a name="handle-unicode-strings"></a>Manipular cadeias de caracteres Unicode

O IDNA dá suporte à transformação de cadeias de caracteres Unicode em rótulos de nome de host legítimos, com exceção das cadeias de caracteres que contêm determinados personagens proibidos, como caracteres de controle, caracteres da área de uso particular (PUA) e similares. Seu aplicativo pode usar o \_ sinalizador de uso de \_ regras STD3 ASCII de IDN \_ \_ com várias funções de conversão NLS para forçar a falha das funções se elas encontrarem caracteres ASCII que não sejam letras, números ou o caractere hífen-subtração (-), ou se uma cadeia de caracteres começar ou terminar com o caractere hífen-subtração. Esses caracteres sempre foram proibidos de serem usados em nomes de domínio e permanecem proibidos no padrão de rascunho.

## <a name="handle-unassigned-code-points"></a>Manipular pontos de código não atribuídos

IDNs não podem conter pontos de código não atribuídos. Portanto, os pontos de código que não estão associados a um caractere ("atribuído") a partir de Unicode 3,2 não têm mapeamentos IDN definidos, embora o \_ sinal de permissão Allow \_ não atribuído em determinadas funções de conversão permita que eles sejam mapeados para Punycode. Você pode encontrar uma lista de pontos de código não atribuídos no [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Se o seu aplicativo codifica pontos de código não atribuídos como Punycode, os nomes de domínio resultantes devem ser ilegais. A segurança poderá ser comprometida se uma versão mais recente do IDNA tornar esses nomes legais ou se o aplicativo filtrar os caracteres ilegais para tentar criar um nome de domínio legal.

 

Pontos de código não atribuídos não são permitidos nas cadeias de caracteres armazenadas usadas em identificadores de protocolo e entidades nomeadas, como nomes em certificados digitais e partes de nome de domínio DNS. No entanto, os pontos de código são permitidos em cadeias de caracteres de consulta, por exemplo, nomes inseridos pelo usuário para autoridades de certificação digitais e pesquisas de DNS, que são usadas para corresponder a identificadores armazenados.

> [!Caution]  
> Embora as cadeias de caracteres de consulta possam usar pontos de código não atribuídos, você não deve usá-las em seus aplicativos. Até mesmo uma cadeia de caracteres de consulta fornecida pelo usuário apresenta um risco de um ataque de "falsificação". Nesse tipo de ataque, o site de host inescrupuloso redireciona os usuários do site que eles pretendem acessar para outro site que pode fornecer informações confidenciais a terceiros. Por exemplo, copiar uma cadeia de caracteres de um email de entrada pode apresentar os mesmos riscos que clicar em um link em um navegador.

 

## <a name="convert-domain-names-to-ascii-names"></a>Converter nomes de domínio em nomes ASCII

Seu aplicativo pode usar a função [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) e determinadas funções de mitigação para converter IDNs em ASCII.

> [!Caution]  
> Como as cadeias de caracteres com representações binárias muito diferentes podem ser comparadas como idênticas, essa função pode gerar certas preocupações de segurança. Para obter mais informações, consulte a discussão sobre funções de comparação em [considerações de segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="examples"></a>Exemplos

[NLS: o exemplo de conversão de IDN (nome de domínio internacionalizado)](nls--internationalized-domain-name--idn--conversion-sample.md) demonstra o uso das funções de conversão de IDN. [NLS: o exemplo de mitigação de IDN (nome de domínio internacionalizado)](nls--internationalized-domain-name--idn--mitigation-sample.md) demonstra o uso das funções de mitigação de IDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md)
</dt> </dl>

 

 



