---
description: alguns aplicativos, como o microsoft Active Directory, o microsoft Exchange e o microsoft Access, mantêm um banco de dados classificável de cadeias de caracteres de localidade e idioma indexadas por nome (cadeia de caracteres UTF-16) e seus pesos de classificação associados.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Lidando com a classificação em seus aplicativos
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 73c7ca897cb5f83e5a073205341f8b0d0f96ff2d0a9d4c7144a914cd5c96c44d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822686"
---
# <a name="handling-sorting-in-your-applications"></a>Lidando com a classificação em seus aplicativos

alguns aplicativos, como o microsoft Active Directory, o microsoft Exchange e o microsoft Access, mantêm um banco de dados classificável de cadeias de caracteres de localidade e idioma indexadas por nome (cadeia de caracteres UTF-16) e seus pesos de classificação associados.

A [classificação](sorting.md) é geralmente intuitiva para os usuários em suas próprias localidades. No entanto, ele pode ser não intuitivo para desenvolvedores de aplicativos. Este tópico discute considerações para lidar com a classificação em seus aplicativos. A classificação pode ser lingüística ou ordinal (não lingüística).

## <a name="sorting-functions"></a>Classificando funções

Você pode usar uma variedade de funções de classificação em seus aplicativos:

-   Funções de comparação de cadeia de caracteres NLS. Os exemplos são [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)e [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal). Consulte [considerações de segurança: recursos internacionais](security-considerations--international-features.md) para obter uma discussão sobre problemas de segurança relacionados às funções de comparação de cadeias de caracteres.
-   Funções de wrapper que chamam internamente as funções de comparação de cadeia de caracteres. As funções mais comuns são [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), que chamam [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw).

Normalmente, as funções de classificação avaliam o caractere de cadeias de caracteres por caractere. No entanto, muitas linguagens têm elementos de vários caracteres, como o par de dois caracteres "CH" em espanhol tradicional. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) use o identificador de localidade fornecido pelo aplicativo ou o nome para identificar elementos de vários caracteres. Em contraste, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) usam a localidade do usuário.

Outro exemplo é vietnamita, que contém muitos elementos de dois caracteres, como as formas maiúsculas, maiúsculas e minúsculas válidas de "GI", que são "GI," Gi "e" Gi ", respectivamente. Qualquer um desses formulários é tratado como um único elemento de classificação e, se o uso de maiúsculas e minúsculas for ignorado, será comparado como igual. No entanto, como "gI" não é válido como um único elemento, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) tratam "Gi" como dois elementos separados.

As funções [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) usam como padrão uma técnica de "classificação de palavras". Para esse tipo de classificação, todas as marcas de Pontuação e outros caracteres não alfanuméricos, exceto o hífen e o apóstrofo, são apresentados antes de qualquer caractere alfanumérico. O hífen e o apóstrofo são tratados de forma diferente dos outros caracteres não alfanuméricos para garantir que palavras como "Coop" e "co-op" permaneçam juntas em uma lista classificada.

Em vez de uma classificação de palavras, o aplicativo pode solicitar uma técnica de "classificação de cadeia de caracteres" das funções de classificação especificando o sinalizador de classificação \_ STRINGSORT. Uma classificação de cadeia de caracteres trata o hífen e o apóstrofo, assim como qualquer outro caractere não alfanumérico. Suas posições na sequência de classificação são anteriores aos caracteres alfanuméricos.

A tabela a seguir compara os resultados de uma classificação de palavra com os resultados de uma classificação de cadeia de caracteres. 

| Classificação de palavras | Classificação de cadeia de caracteres |
|-----------|-------------|
| billet    | da fatura      |
| compõe     | billet      |
| da fatura    | compõe       |
| não pode    | possível       |
| conseguir      | não pode      |
| possível     | conseguir        |
| telefonema       | cooperação       |
| coop      | telefonema         |
| cooperação     | coop        |



 

## <a name="sort-strings-linguistically"></a>Classificar cadeias de caracteres linguísticamente

As funções [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) são testadas para igualdade lingüística. Seus aplicativos devem usar essas funções com a localidade correta para classificar cadeias de caracteres lingüísticas.

> [!Note]  
> Para compatibilidade com o Unicode, um aplicativo deve preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ou a versão Unicode de [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Outro motivo para preferir [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) é que a Microsoft está migrando para o uso de nomes de localidade em vez de identificadores de localidade para novas localidades, por motivos de interoperabilidade. qualquer aplicativo que é executado somente no Windows Vista e posterior deve usar [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Outra maneira de testar a igualdade lingüística é usar [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), que sempre usam uma classificação de palavras. A função [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) chama o [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) com o \_ sinalizador normal IGNORECASE, enquanto [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) o chama sem esse sinalizador. Para obter uma visão geral do uso das funções de wrapper, consulte [**cadeias de caracteres**](../menurc/strings.md).

As funções recuperam resultados linguísticamente apropriados para todas as localidades. As expectativas do usuário para diferentes localidades podem diferir significativamente no comportamento de classificação, conforme mostrado nos exemplos a seguir.

-   Muitas localidades correspondem à ligadura AE (æ) com as letras ae. No entanto, a Islandês (Islândia) considera uma letra separada e a coloca após Z na sequência de classificação.
-   O anel (Å) normalmente classifica com apenas uma diferença de sinais diacríticos de um. No entanto, Sueco (Suécia) coloca o anel após Z na sequência de classificação.

As funções tentam verificar rigorosamente que os pontos de código definidos no padrão Unicode são, de forma canônica, igual a uma cadeia de caracteres de pontos de código equivalentes. Por exemplo, o ponto de código que representa um "u" minúsculo com um ditrema (ü) é canônicamente igual a um "u" minúsculo, combinado com os caracteres de trema (̈). Observe, no entanto, que a equivalência canônica nem sempre é possível.

como quase todos os dados inseridos usando os teclados Windows e imes (input method editors) estão em conformidade com a normalização de C do formulário definida no padrão Unicode, a conversão de dados de entrada de outras plataformas usando as funções de normalização do NLS Unicode fornece resultados mais consistentes, especialmente para localidades que usam o script tibetano ou o script hangul para o hangul moderno. para obter mais informações sobre o suporte de normalização unicode no Windows Vista e posterior, consulte [usando a normalização unicode para representar cadeias de caracteres](using-unicode-normalization-to-represent-strings.md).

Quando a comparação de cadeias de caracteres segue a preferência de idioma do usuário, por exemplo, ao classificar itens para um controle ListView ordenado, o aplicativo pode executar um dos seguintes procedimentos:

-   Chame [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) com a localidade do usuário.
-   Chame [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) para definir uma localidade para a comparação, para passar sinalizadores adicionais, para inserir caracteres nulos ou para passar comprimentos explícitos para corresponder a partes de uma cadeia de caracteres.

Quando os resultados da comparação devem ser consistentes, independentemente da localidade, por exemplo, ao comparar dados recuperados em uma lista predefinida ou um valor interno, o aplicativo deve usar [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) com o parâmetro *LOCALE* definido como \_ invariável locale. Para [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), qualquer uma das seguintes chamadas será correspondente mesmo se MyStr for "INLAP". Nesse caso, uma chamada de localidade sensível a [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) falhará se a localidade atual for vietnamita.

No Windows XP:


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Em sistemas operacionais anteriores:


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Classificar cadeias de caracteres no ordinal

Para classificação Ordinal (não lingüística), seus aplicativos sempre devem usar a função [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .

> [!Note]  
> essa função só está disponível para o Windows Vista e posterior.

 

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) compara duas cadeias de caracteres [Unicode](unicode.md) para testar a igualdade binária, em oposição à igualdade linguística. Exemplos de tais cadeias de caracteres não linguísticas são nomes de arquivo NTFS, variáveis de ambiente e nomes de mutexes, pipes nomeados ou processadores de bits. Exceto pela opção de não diferenciação de maiúsculas e minúsculas, essa função desconsidera todas as equivalências não binárias. Ao contrário de algumas outras funções de classificação, ele testa todos os pontos de código para igualdade, incluindo aqueles que não recebem nenhum peso nos esquemas de classificação linguística.

Todas as instruções a seguir se aplicam a [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) em comparações binárias, mas não a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   Sequências equivalentes canônicas em Unicode, como letra latina minúscula A com anel superior (U + 00e5) e letra latina minúscula A + combinação de anel superior (U + 0061 U + 030a), não são iguais, mesmo que pareçam idênticas ("å").
-   Cadeias de caracteres canônicos canônicas em Unicode, como Letra Latina Versalete Y (U + 028f) e letra latina maiúscula Y (U + 0059), que parecem muito semelhantes ("ʏ" e "Y") e variam apenas por alguns pesos de caso especiais nas tabelas linguísticas, são considerados caracteres totalmente diferentes. Mesmo que o aplicativo defina *bIgnoreCase* como **true**, essas cadeias de caracteres se compararão como diferentes.
-   Os pontos de código definidos mas não têm peso de classificação linguístico, como a junção de largura ZERO (U + 200D), são tratados como tendo seus pesos de ponto de código.
-   Os pontos de código definidos em versões posteriores do Unicode, mas sem peso nas tabelas linguística atuais, são tratados como tendo seus pesos de ponto de código.
-   Pontos de código que são indefinidos por Unicode são tratados como tendo seus pesos de ponto de código.
-   Quando o aplicativo define *bIgnoreCase* como **true**, a função mapeia o caso usando a tabela de uso em maiúsculas do sistema operacional, em vez das informações nas tabelas de classificação linguística. Portanto, o mapeamento é independente da localidade.

Para obter mais informações sobre sequências equivalentes canônicas em Unicode e cadeias de caracteres comuns semelhantes em Unicode, consulte [usando a normalização Unicode para representar cadeias de caracteres](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Classificar pontos de código

Alguns pontos de código Unicode não têm peso, por exemplo, sem junção de largura ZERO, U + 200C. As funções de classificação avaliam intencionalmente os pontos de código sem peso como equivalentes porque não têm peso na classificação. no Windows Vista e posterior, o aplicativo pode classificar esses pontos de código chamando as funções de comparação de cadeia de caracteres NLS, particularmente [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), para avaliação de todos os pontos de código em um sentido literal, por exemplo, na validação de senha. em sistemas operacionais anteriores ao Windows Vista, o aplicativo deve usar a função de tempo de execução C **strcmp** ou **wcscmp**.

As funções de classificação ignoram diacríticos, como não ESPAÇAmento BRAQUIA, U + 0306, quando o aplicativo especifica o sinalizador de não espaço de Hlink \_ . Da mesma forma, essas funções ignoram símbolos, por exemplo, sinal de igual, U + 003D, quando o \_ sinalizador de símbolos Hlink é especificado. No Windows Vista e posterior, o aplicativo chama [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) para avaliação de diacríticas e pontos de código de símbolo em um sentido literal binário. Em sistemas operacionais Windows Vista, o aplicativo deve usar **strcmp** ou **wcscmp**.

Alguns pontos de código, como 0xFFFF e 0x058b, atualmente não são atribuídos em Unicode. Esses pontos de código não recebem nenhum peso na classificação e nunca devem ser passados para as funções de classificação. O aplicativo deve usar [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) para detectar pontos de código não Unicode em um fluxo de dados.

> [!Note]  
> Os resultados de [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) podem variar dependendo da versão Unicode passada se um caractere for adicionado ao Unicode em uma versão posterior e posteriormente adicionado às tabelas de classificação Windows dados. Para obter mais informações, consulte [Usar o sort versioning](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Classificar dígitos como números

No Windows 7 e posterior, o aplicativo pode chamar [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**LCMapString ou**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) usando o sinalizador SORT \_ DIGITSASNUMBERS. Esse sinalizador dá suporte à classificação que trata dígitos como números, por exemplo, classificação de "2" antes de "10".

Observe que o uso desse sinalizador não é apropriado para dígitos hexadecimais, como o seguinte. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

Nesse caso, os "números" são classificação em ordem, mas o usuário percebe uma lista hexadecimal mal classificação.

## <a name="map-strings"></a>Mapear cadeias de caracteres

O aplicativo usa a [**função LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) para mapear cadeias de caracteres, se LCMAP \_ SORTKEY não for especificado. Uma cadeia de caracteres mapeada será terminada em nulo se a cadeia de caracteres de origem for terminada em nulo.

Ao transformar entre maiúsculas e minúsculas, a função não garante que um único caractere será mapeando para um único caractere. Por exemplo, os sinalizadores LCMAP LOWERCASE e LCMAP UPPERCASE podem mapear o \_ \_ sharp S alemão ("ª") para si mesmo. Como alternativa, o sinalizador LCMAP UPPERCASE pode mapear "ª" para "SS" e o sinalizador LCMAP LOWERCASE pode mapear \_ \_ "SS" para "ª". O comportamento depende da versão do NLS.

Ao transformar entre maiúsculas e minúsculas, a função não é sensível ao contexto. Por exemplo, embora o sinalizador LCMAP UPPERCASE mapeie corretamente sigma em letras minúsculas gregos ("σ") e sigma final em minúsculas grego ("σ") para sigma maiúsculas gregos ("Σ"), o sinalizador LCMAP LOWERCASE sempre mapeia \_ \_ "Σ" para "σ", nunca para "Σ".

Por padrão, a função mapeia o "i" em letras minúsculas para o "I" em letras maiúsculas, mesmo quando o parâmetro *Locale* especifica turco ou Turco. Para substituir esse comportamento para turco ou Turco, o aplicativo deve especificar LCMAP \_ LINGUISTIC \_ CASING. Se esse sinalizador for especificado com a localidade apropriada, "fk" (I sem ponto minúsculo) será a forma minúscula de "I" (I sem ponto em maiúsculas) e "i" (I pontilhado em minúsculas) será a forma minúscula de "2" (I pontilhado em maiúscula).

Se o sinalizador LCMAP HIRAGANA for especificado para mapear caracteres katakana para caracteres \_ hiragana e LCMAP FULLWIDTH não for \_ especificado, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mapeará apenas caracteres de largura inteira para hiragana. Nesse caso, todos os caracteres katakana de meia largura são colocados como na cadeia de caracteres de destino, sem mapeamento para hiragana. O aplicativo deve especificar LCMAP FULLWIDTH para mapear caracteres katakana de meia \_ largura para hiragana. O motivo dessa restrição é que todos os caracteres hiragana são caracteres de largura inteira.

Se o aplicativo precisar retirar caracteres da cadeia de caracteres de origem, ele poderá chamar a função de mapeamento com os sinalizadores NORM \_ IGNORESYMBOLS e NORM IGNORENONSPACE definidos e todos os outros sinalizadores \_ limpos. Se o aplicativo fizer isso com uma cadeia de caracteres de origem que não seja terminada em nulo, será possível que a função retorne uma cadeia de caracteres vazia e não retorne um erro.

## <a name="create-sort-keys"></a>Criar chaves de classificação

Quando o aplicativo especifica LCMAP \_ SORTKEY, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) gera uma chave de classificação, uma matriz binária de valores de byte. A chave de classificação não é uma cadeia de caracteres verdadeira e seus valores representam o comportamento de classificação da cadeia de caracteres de origem, mas não são valores de exibição significativos.

> [!Note]  
> A função ignora o kashida árabe durante a geração de uma chave de classificação. Se um aplicativo chamar a função para criar uma chave de classificação para uma cadeia de caracteres que contém um kashida árabe, a função não criará nenhum valor de chave de classificação.

 

A chave de classificação pode conter um número ímpar de bytes. O sinalizador LCMAP \_ BYTEREV inverte apenas um número de bytes. O último byte (ímpar) na chave de classificação não é invertido. Se o byte 0x00 de terminação for um byte de posição ímpar, ele permanecerá o último byte na chave de classificação. Se o byte 0x00 de terminação for um byte com posição even, ele trocará posições com o byte que o precede.

Ao gerar a chave de classificação, a função trata o hífen e o apóstrofo de forma diferente de outros símbolos de pontuação, de modo que palavras como "meu" e "cooperação" permaneçam juntas em uma lista. Todos os símbolos de pontuação diferentes do hífen e do apóstrofo são classificação antes de caracteres alfanuméricos. O aplicativo pode alterar esse comportamento definindo o sinalizador SORT \_ STRINGSORT, conforme descrito [em Funções de Classificação](#sorting-functions).

Quando usada no [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp), a chave de classificação produz a mesma ordem de quando a cadeia de caracteres de origem é usada em [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx.**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) A [função memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) deve ser usada em vez [de strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), porque a chave de classificação pode ter bytes nulos inseridos.

## <a name="use-sort-versioning"></a>Usar o versionamento de classificação

Uma [tabela de](sorting.md) classificação tem dois números que identificam sua versão: a versão definida e a versão NLS. Ambos os números são valores DWORD, compostos por um valor principal e um valor secundário. O primeiro byte de um valor é reservado, os próximos dois bytes representam a versão principal e o último byte representa a versão secundária. Em termos hexadecimais, o padrão é 0xRRMMMMmm, em que R é igual a Reservado, M é igual a principal e m é menor. Por exemplo, uma versão principal de 3 com uma versão secundária de 4 é representada como 0x304.

A versão definida identifica opertoire de pontos de código e é a mesma para todas as localidades. A versão principal é incrementada para indicar alterações nos pontos de código existentes. A versão secundária é incrementada para indicar que os pontos de código foram adicionados, mas que nenhum ponto de código existente anteriormente foi alterado.

A versão NLS é específica para [](locale-names.md)um [identificador](locale-identifiers.md) de localidade ou nome de localidade e rastreia as alterações nos pesos do ponto de código para a localidade afetada. A versão principal é incrementada quando os pesos são alterados para pontos de código que já eram sortíveis. A versão secundária é incrementada quando novos pontos de código são atribuídos a pesos, mas todos os outros pesos de ponto de código anteriormente sortíveis permanecem inalterados.

> [!Note]  
> Para uma versão principal, um ou mais pontos de código são alterados para que o aplicativo deve indexar todos os dados para que as comparações sejam válidas. Para uma versão secundária, nada é movido, mas os pontos de código são adicionados. Para esse tipo de versão, o aplicativo só precisa indexar as cadeias de caracteres com valores anteriormente insumentáveis.

 

> [!IMPORTANT]
> A versão principal foi alterada em Windows 8. Os dados criados em versões Windows anteriores devem ser indexados.

 

As versões definidas e NLS se aplicam a pontos de código sortíveis recuperados usando a função [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) com o sinalizador SORTKEY de LCMAP e também usadas pelas funções \_ [**CompareString,**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) [**CompareStringEx,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)e [**FindNLSStringEx.**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) Se um ou mais pontos de código em uma cadeia de caracteres são não ortáveis, a função [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) retorna **FALSE** quando essa cadeia de caracteres é passada para ela como um parâmetro.

O aplicativo pode chamar [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) ou [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) para recuperar a versão definida e a versão NLS de uma tabela de classificação.

## <a name="index-the-database"></a>Indexar o banco de dados

Por motivos de desempenho, o aplicativo deve seguir este procedimento ao indexar o banco de dados.

**Para indexar corretamente o banco de dados**

1.  Para cada função, armazene a versão NLS, as chaves de classificação dessa versão e uma indicação de classificação para cada cadeia de caracteres indexada.
2.  Quando a versão secundária é incrementada, indexe as cadeias de caracteres anteriormente não reormentáveis. As cadeias de caracteres afetadas nessa atualização devem ser limitadas às que [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) retornou **anteriormente FALSE.**
3.  Quando a versão principal é incrementada, re indexe todas as cadeias de caracteres porque os pesos atualizados podem alterar o comportamento de qualquer cadeia de caracteres. As versões principais são muito pouco frequentes.

Problemas de indexação de banco de dados podem surgir pelos seguintes motivos:

-   Um sistema operacional posterior pode definir pontos de código indefinido para um sistema operacional anterior, alterando a classificação.
-   Os pontos de código podem ter pesos de classificação diferentes em diferentes sistemas operacionais, devido a correções no suporte ao idioma.

Para minimizar a necessidade de indexar o banco de dados nessas circunstâncias, o aplicativo pode usar [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) para diferenciar as cadeias de caracteres indefinidas para que o aplicativo possa rejeitar cadeias de caracteres com pontos de código indefinido. O uso [**de GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) ou [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) permite que o aplicativo determine se uma alteração de NLS afeta a localidade usada para uma tabela de índice específica. Se a alteração não tiver nenhum efeito na localidade, o aplicativo não precisará indexar a tabela de novo.

## <a name="examples"></a>Exemplos

A tabela a seguir ilustra os efeitos de determinados sinalizadores usados com as funções de classificação. Em cada caso, a seleção de sinalizadores determina se dois caracteres diferentes são considerados iguais para fins de classificação.



| Caractere 1                                                        | Caractere 2                                             | Padrão | NORM \_ IGNOREWIDTH | NORM \_ IGNOREKANA | NORM \_ IGNOREWIDTH\| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U+3042 HIRAGANA LETRA A<br/>                | "ガ"<br/> U+30A2 KATAKANA LETRA A<br/>     | Desiguais | Desiguais           | Igual            | Igual                              |
| "ｵ"<br/> LETRA KATAKANA U + FF75 DE MEIA LARGURA<br/>       | "オ"<br/> U + 30AA LETRA KATAKANA O<br/>     | Desiguais | Igual             | Desiguais          | Igual                              |
| B<br/> U + LETRA LATINA MAIÚSCULA FF22 MINÚSCULA B<br/> | "B"<br/> U + 0042 LETRA LATINA MAIÚSCULA B<br/> | Desiguais | Igual             | Desiguais          | Igual                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Classificação](sorting.md)
</dt> <dt>

[Recuperando e definindo informações de localidade](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Usando a normalização Unicode para representar cadeias de caracteres](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
