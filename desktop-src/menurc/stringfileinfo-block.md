---
title: Instrução StringFileInfo BLOCK
description: Descreve a forma do bloco de informações de cadeia de caracteres.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Menus de instrução StringFileInfo BLOCK e outros recursos
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0a1c5e7a2fd5e3d2f096c882ca928ce1febf92
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364876"
---
# <a name="stringfileinfo-block-statement"></a>Instrução StringFileInfo BLOCK

Define um bloco de informações de cadeia de caracteres.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Par de identificador de conjunto de caracteres e idioma. É uma cadeia de caracteres hexadecimal que consiste na concatenação do idioma e dos identificadores de conjunto de caracteres especificados na seção de comentários.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nome da cadeia de caracteres*
</dt> <dd>

Nome de um valor no bloco e pode ser um dos nomes predefinidos especificados na seção comentários.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Cadeia de caracteres que especifica o valor do nome da cadeia de caracteres correspondente. Mais de uma instrução **Value** pode ser fornecida.

</dd> </dl>

## <a name="remarks"></a>Comentários

O parâmetro *Lang-charset* especifica um dos seguintes códigos de idioma.



| Código   | Idioma            | Código   | Idioma                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Árabe              | 0x0415 | Polonês                    |
| 0x0402 | Búlgaro           | 0x0416 | Português (Brasil)       |
| 0x0403 | Catalão             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinês tradicional | 0x0418 | Romeno                  |
| 0x0405 | Tcheco               | 0x0419 | Russo                   |
| 0x0406 | Dinamarquês              | 0x041A | Croato-Serbian (latino)    |
| 0x0407 | Alemão              | 0x041B | Eslovaco                    |
| 0x0408 | Grego               | 0x041C | Albanês                  |
| 0x0409 | Inglês americano        | 0x041D | Sueco                   |
| 0x040A | Castelhano espanhol   | 0x041E | Tailandês                      |
| 0x040B | Finlandês             | 0x041F | Turco                   |
| 0x040C | Francês              | 0x0420 | Urdu                      |
| 0x040D | Hebraico              | 0x0421 | Bahasa                    |
| 0x040E | Húngaro           | 0x0804 | Chinês simplificado        |
| 0x040F | Islandês           | 0x0807 | Alemão suíço              |
| 0x0410 | Italiano             | 0x0809 | Inglaterra Inglês              |
| 0x0411 | Japonês            | 0x080A | Espanhol (México)          |
| 0x0412 | Coreano              | 0x080C | Francês belga            |
| 0x0413 | Holandês               | 0x0C0C | Francês do Canadá           |
| 0x0414 | Norueguês – Bokmal  | 0x100C | Francês suíço              |
| 0x0810 | Italiano suíço       | 0x0816 | Português (Portugal)     |
| 0x0813 | Holandês belga       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Norueguês – Nynorsk | ?      | ?                         |



 

O parâmetro *Lang-charset* também especifica um dos seguintes identificadores de conjunto de caracteres.



| Identificador | Conjunto de caracteres              |
|------------|----------------------------|
| 0          | ASCII de 7 bits                |
| 932        | Japão (Shift – JIS X-0208) |
| 949        | Coreia (Shift – KS 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latim-2 (Europa Oriental) |
| 1251       | Cirílico                   |
| 1252       | Multilíngüe               |
| 1253       | Grego                      |
| 1254       | Turco                    |
| 1255       | Hebraico                     |
| 1256       | Árabe                     |



 

O parâmetro de *nome de cadeia de caracteres* especifica um dos seguintes nomes predefinidos.



| Nome                 | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentários**         | Informações adicionais que devem ser exibidas para fins de diagnóstico.                                                                                                                                                                                                                                    |
| **CompanyName**      | Empresa que produziu o arquivo — por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc." Essa cadeia de caracteres é necessária.                                                                                                                                                                   |
| **FileDescription**  | Descrição do arquivo a ser apresentado aos usuários. Essa cadeia de caracteres pode ser exibida em uma caixa de listagem quando o usuário estiver escolhendo arquivos a serem instalados — por exemplo, "driver de teclado para AT-Style teclados". Essa cadeia de caracteres é necessária.                                                                                            |
| **FileVersion**      | Número de versão do arquivo — por exemplo, "3,10" ou "5,00. RC2". Essa cadeia de caracteres é necessária.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno do arquivo, se houver um — por exemplo, um nome de módulo se o arquivo for uma biblioteca de vínculo dinâmico. Se o arquivo não tiver um nome interno, essa cadeia de caracteres deverá ser o nome de arquivo original, sem extensão. Essa cadeia de caracteres é necessária.                                                                       |
| **LegalCopyright**   | Avisos de direitos autorais que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais e assim por diante. Essa cadeia de caracteres é opcional.                                                                                                                                             |
| **LegalTrademarks**  | Marcas registradas e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante. Essa cadeia de caracteres é opcional.                                                                                                                        |
| **OriginalFilename** | Nome original do arquivo, sem incluir um caminho. Essas informações permitem que um aplicativo determine se um arquivo foi renomeado por um usuário. O formato do nome depende do sistema de arquivos para o qual o arquivo foi criado. Essa cadeia de caracteres é necessária.                                                 |
| **PrivateBuild**     | Informações sobre uma versão particular do arquivo — por exemplo, "compilado por TESTER1 em \\ TESTBED". Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ PRIVATEBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz.                                                                                   |
| **ProductName**      | Nome do produto com o qual o arquivo é distribuído. Essa cadeia de caracteres é necessária.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versão do produto com a qual o arquivo é distribuído — por exemplo, "3,10" ou "5,00. RC2". Essa cadeia de caracteres é necessária.                                                                                                                                                                                       |
| **SpecialBuild**     | Texto que especifica como esta versão do arquivo difere da versão padrão — por exemplo, "compilação particular para resolver problemas do mouse em M250 e M250E computadores". Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ SPECIALBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz. |



 

 

 




