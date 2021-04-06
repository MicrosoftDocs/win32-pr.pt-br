---
description: Este tópico descreve como o Windows Search dá suporte a vários idiomas.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Idiomas com suporte do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646883"
---
# <a name="languages-supported-by-windows-search"></a>Idiomas com suporte do Windows Search

Este tópico descreve como o Windows Search dá suporte a vários idiomas.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Geração de tokens, separadores e recursos de idioma

A pesquisa do Windows é independente de linguagem, mas a precisão da pesquisa entre linguagens pode variar devido à maneira como separadores o texto de token. Separadores implementam várias regras de geração de tokens para idiomas e dividem o texto em tokens individuais, ou palavras, para serem indexados ou pesquisados.

O idioma do texto indexado e a cadeia de caracteres de consulta são divididos em tokens. Como as regras de geração de tokens variam por idioma, há separadores separadas para cada idioma ou família de idiomas. Se houver uma incompatibilidade entre a linguagem de consulta e a linguagem indexada, os resultados poderão ser imprevisíveis.

O Windows Search é fornecido com um conjunto bem definido de separadores. Os componentes de separador de separador clássico e lematizador têm suporte no Windows Vista e versões posteriores. Se o idioma de um documento não puder ser determinado, o Windows Search tentará detectar o idioma para identificar o separador de repetições mais apropriado. O Windows Search tenta detectar o idioma chamando a função [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) para determinar a primeira linguagem MUI (interface de usuário múltiplo) (que normalmente é o idioma da interface do usuário do sistema, a menos que os pacotes de idiomas MUI estejam instalados). Se essa chamada for realizada com sucesso, o separador de primeira linguagem MUI será usado. Se a chamada para **GetSystemPreferredUILanguages** falhar, o Windows Search recuperará a localidade do sistema chamando a função [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) e usará o separador associado a essa localidade.

Se nenhum separador de documentos for instalado para um idioma, a pesquisa do Windows será interrompida em espaço em branco usando o separador **neutro** .

Você pode remover um idioma por meio do registro, conforme ilustrado no exemplo a seguir.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Se você fizer alterações no registro, reinicie o Windows Search.

 

Quando o Windows Search exige um novo separador de itens, o CLSID (identificador de classe) é lido e o separador de separações instanciado é armazenado em cache.

Você pode criar um separador de separador personalizado para um idioma implementando a interface [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) . Em seguida, o Windows Search chama os métodos **IWordBreaker** quando cria índices de conteúdo e executa consultas.

As informações de localidade do conteúdo indexado são recuperadas da origem do conteúdo. Se o implementador de origem não souber a localidade do conteúdo indexado, ele deverá definir a localidade como [**\_ neutra de localidade**](../intl/locale-neutral.md).

Por exemplo, se você implementar um manipulador de filtro (uma implementação da interface [**IFilter**](https://www.bing.com/search?q=**IFilter**) ), manipulador de propriedades ou manipulador de protocolo, deverá definir a localidade para conteúdo indexado para [**localidade \_ neutra**](../intl/locale-neutral.md) , a menos que você tenha informações de localidade específicas e esteja confiante de sua exatidão.

> [!TIP]
> Se uma consulta de índice for baseada na entrada do usuário, a localidade deverá corresponder ao idioma no qual o usuário está digitando. Você pode determinar essa localidade chamando a função [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) .

 

## <a name="languages-supported-by-wordbreakers"></a>Idiomas com suporte do separadores

O Windows Search inclui o separadores para dar suporte aos seguintes idiomas.



| Chave do Registro             | Idioma (subidioma)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_SaudiArabia árabe**  | Árabe (neutro)                                  | 0x0001 |
| **Padrão de Bengali \_**     | Bengali (neutro)                                  | 0x0045 |
| **\_Padrão búlgaro**   | Búlgaro (Bulgária)                              | 0x0402 |
| **\_Padrão catalão**     | Catalão (Catalunha)                                 | 0x0403 |
| **\_Hong Kong Chinês**    | Chinês (RAE de Hong Kong, RPC)                      | 0x0C04 |
| **Chinês \_ simplificado**  | Chinês (Simplificado)                              | 0x0804 |
| **Chinês \_ tradicional** | Chinês (Tradicional)                             | 0x0404 |
| **\_Padrão Croata**    | Croata (Croácia)                                | 0x041A |
| **\_Padrão tcheco**       | Tcheco (República Tcheca)                            | 0x0405 |
| **\_Padrão dinamarquês**      | Dinamarquês (Dinamarca)                                  | 0x0406 |
| **Holandês \_ -holandês**         | Holandês (Países Baixos)                               | 0x0413 |
| **Inglês ( \_ Reino Unido)**          | Inglês (Reino Unido)                          | 0x0809 |
| **Inglês \_ dos EUA**          | Inglês (Estados Unidos)                           | 0x0409 |
| **\_Padrão finlandês**     | Finlandês (Finlândia)                                 | 0x040B |
| **Francês \_ francesa**       | Francês (França)                                   | 0x040C |
| **Alemão \_ alemão**       | Alemão (Alemanha)                                  | 0x0407 |
| **\_Padrão grego**       | Grego (Grécia)                                    | 0x0408 |
| **\_Padrão Guzerate**    | Gujarati (Índia)                                  | 0x0447 |
| **\_Padrão Hebraico**      | Hebraico (neutro)                                  | 0x000D |
| **\_Padrão Hindi**       | Híndi (Índia)                                     | 0x0439 |
| **\_Padrão húngaro**   | Húngaro (Hungria)                               | 0x040E |
| **Padrão de Islandês \_**   | Islandês (Islândia)                               | 0x040F |
| **Padrão de indonésio \_**  | Indonésio (Indonésia)                            | 0x0421 |
| **Italiano \_ italiano**     | Italiano (Itália)                                   | 0x0410 |
| **\_Padrão japonês**    | Japonês (Japão)                                  | 0x0411 |
| **Padrão de Kannada \_**     | canarim (Índia)                                   | 0x044B |
| **\_Padrão coreano**      | Coreano (Coreia do Sul)                                    | 0x0412 |
| **\_Padrão Letão**     | Letão (Letônia)                                  | 0x0426 |
| **\_Padrão lituano**  | Lituano (Lituano)                           | 0x0427 |
| **Malaio \_ Malásia**      | Malaio (Malásia)                                  | 0x043E |
| **\_Padrão malaiala**   | Malaiala (neutro)                               | 0x004C |
| **Padrão marata \_**     | Marati (Índia)                                   | 0x044E |
| **Norueguês \_ Bokmal**    | Norueguês, (Bokmål, Noruega)                        | 0x0414 |
| **\_Padrão polonês**      | Polonês (Polônia)                                   | 0x0415 |
| **Português do \_ Portugal** | Português (Portugal)                             | 0x0816 |
| **Português do \_ Brasil**   | Português (Brasil)                               | 0x0416 |
| **Padrão de Punjabi \_**     | panjabi (Índia)                                   | 0x0446 |
| **\_Padrão romeno**    | Romeno (Romênia)                                | 0x0418 |
| **\_Padrão russo**     | Russo (neutro)                                 | 0x0019 |
| **Sérvio \_ cirílico**    | Sérvio (Sérvia e Montenegro, antiga, cirílico) | 0x0C1A |
| **Sérvio \_ latino**       | Sérvio (Sérvia e Montenegro, antiga, latino)    | 0x081A |
| **\_Padrão eslovaco**      | Eslovaco (Eslováquia)                                 | 0x041B |
| **\_Padrão esloveno**   | Esloveno (Eslovênia)                              | 0x0424 |
| **Espanhol \_ moderno**      | Espanhol (Espanha, classificação moderna)                      | 0x0C0A |
| **\_Padrão Sueco**     | Sueco (Suécia)                                  | 0x041D |
| **Padrão de tâmil \_**       | Tâmil (Índia)                                     | 0x0449 |
| **Padrão de télugo \_**      | Télugo (Índia)                                    | 0x044A |
| **\_Padrão tailandês**        | Tailandês (Tailândia)                                   | 0x041E |
| **\_Padrão Turco**     | Turco (Turquia)                                  | 0x041F |
| **\_Padrão ucraniano**   | Ucraniano (Ucrânia)                               | 0x0422 |
| **Padrão de urdu \_**        | Urdu (Paquistão)                                   | 0x0420 |
| **\_Padrão vietnamita**  | Vietnamita (Vietnã)                              | 0x042A |



 

> [!Note]  
> Os LCIDs para alguns idiomas na tabela são gerados usando o identificador de idioma, o identificador de subidioma e o identificador de classificação.

 

Para obter mais informações sobre linguagens e identificadores associados, consulte [constantes e cadeias de caracteres de identificador de linguagem](../intl/language-identifier-constants-and-strings.md).

> [!Note]  
> Não há nenhuma garantia de que todas essas chaves de registro de idioma estarão presentes em um determinado computador. O separador de qualquer idioma específico pode ou não ser instalado no computador, dependendo das configurações do usuário.

 

A **partir do Windows 8.1**, a maneira preferida de usar separadores é por meio da [**classe WordsSegmenter**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)da API do WinRT.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como implementar e usar separadores de palavras e lematizadores personalizados para idiomas e localidades adicionais, consulte [estendendo recursos de idioma no Windows Search](extending-language-resources-in-windows-search.md).
-   Se você precisar identificar o idioma de uma parte do texto, poderá usar a detecção automática de idioma (LAD), que está disponível no Windows 7 e posterior. Para obter mais informações, consulte Els ( [Serviços lingüísticos estendidos](../intl/extended-linguistic-services.md) ).
-   Para obter informações sobre como gerenciar, consultar e estender o índice, consulte o [Guia do desenvolvedor do Windows Search](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Usar código gerenciado com os dados do Shell e do Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
