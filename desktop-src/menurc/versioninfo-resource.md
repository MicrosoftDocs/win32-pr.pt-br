---
title: Recurso VERSIONINFO
description: Define um recurso de informações de versão. O recurso contém informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original. O recurso destina-se a ser usado com as funções de informações de versão.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menus de recursos do VERSIONINFO e outros recursos
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "104294587"
---
# <a name="versioninfo-resource"></a>Recurso VERSIONINFO

Define um recurso de informações de versão. O recurso contém informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original. O recurso destina-se a ser usado com as funções de [informações de versão](./version-information.md) .

Há duas maneiras de Formatar uma instrução **VERSIONINFO** :

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- ou –

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

Versão – identificador de recurso de informações. Esse valor deve ser 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*informações fixas*
</dt> <dd>

Informações de versão, como a versão do arquivo e o sistema operacional pretendido. Esse parâmetro consiste nas instruções a seguir.



| Instrução                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  *Versão* da versão         | Número de versão binária do arquivo. A *versão* consiste em inteiros de 2 32 bits, definidos por inteiros de 4 16 bits. Por exemplo, "FileVersion 3, 10, 0, 61" é traduzido em dois doublewords: 0x0003000a e 0x0000003d, nessa ordem. Portanto, se a *versão* for definida pelos valores **DWORD** *dw1* e *DW2*, eles precisarão aparecer na instrução **FileVersion** da seguinte maneira: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` . |
|  *Versão* do PRODUCTVERSION      | Número de versão binária do produto com o qual o arquivo é distribuído. O parâmetro *version* é um número inteiro de 2 32 bits, definido por inteiros de 4 16 bits. Para obter mais informações sobre a *versão*, consulte a descrição de **FileVersion** .                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *FILEFLAGSMASK* | Indica quais bits na instrução **FILEFLAGS** são válidos. Para o Windows de 16 bits, esse valor é 0x3F.                                                                                                                                                                                                                                                                                                                                          |
| *Sinalizadors* de **FILEFLAGS**         | Atributos do arquivo.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS** *FILEOS*               | Sistema operacional para o qual este arquivo foi projetado. O parâmetro *fileos* pode ser um dos valores do sistema operacional fornecidos na seção comentários.                                                                                                                                                                                                                                                                                               |
|  *Filetype* de filetype           | Tipo geral de arquivo. O parâmetro *filetype* pode ser um dos valores de tipo de arquivo listados na seção comentários.                                                                                                                                                                                                                                                                                                                                |
| Subtipo **FILESUBTYPE**          | Função do arquivo. O parâmetro de *subtipo* é zero, a menos que o parâmetro *filetype* na instrução **FILETYPE** seja VFT \_ DRV, VFT \_ Font ou VFT \_ VXD. Para obter uma lista de valores de subtipo de arquivo, consulte a seção comentários.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*instrução Block*
</dt> <dd>

Especifica um ou mais blocos de informações de versão. Um bloco pode conter informações de cadeia de caracteres ou informações de variáveis. Para obter mais informações, consulte bloco [**StringFileInfo**](stringfileinfo-block.md) ou [**bloco VarFileInfo**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar as constantes especificadas com a instrução **VERSIONINFO** , você deve incluir o arquivo de cabeçalho winver. h ou Windows. h no arquivo de definição de recurso.

A lista a seguir descreve os parâmetros usados na instrução **VERSIONINFO** :

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*sinalizadores de*
</dt> <dd>

Uma combinação dos valores a seguir.



| Valor                      | Descrição                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **depuração do VS \_ FF \_**          | O arquivo contém informações de depuração ou é compilado com recursos de depuração habilitados.                                                                                                                                                                                         |
| **com \_ patch do vs FF \_**        | O arquivo foi modificado e não é idêntico ao arquivo de envio original do mesmo número de versão.                                                                                                                                                                       |
| **PRÉ-lançamento do VS \_ FF \_**     | O arquivo é uma versão de desenvolvimento, não um produto lançado comercialmente.                                                                                                                                                                                                         |
| **PRIVATEBUILD do VS \_ FF \_**   | O arquivo não foi compilado usando procedimentos de versão padrão. Se esse valor for fornecido, o [**bloco StringFileInfo**](stringfileinfo-block.md) deverá conter uma cadeia de caracteres **PrivateBuild** .                                                                                              |
| **SPECIALBUILD do VS \_ FF \_**   | O arquivo foi criado pela empresa original usando procedimentos de versão padrão, mas é uma variação do arquivo padrão do mesmo número de versão. Se esse valor for fornecido, o bloco de [bloco **StringFileInfo**](stringfileinfo-block.md) deverá conter uma cadeia de caracteres **SpecialBuild** . |
| **VS \_ FFI \_ FILEFLAGSMASK** | Uma combinação de todos os valores anteriores.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

Um dos valores a seguir.



| Valor                   | Descrição                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ desconhecido**        | O sistema operacional para o qual o arquivo foi projetado é desconhecido. |
| **VOS \_ dos**            | O arquivo foi projetado para o MS-DOS.                                    |
| **VOS \_ NT**             | O arquivo foi projetado para o Windows de 32 bits.                            |
| **VOS \_ \_ WINDOWS16**    | O arquivo foi projetado para o Windows de 16 bits.                            |
| **VOS \_ \_ WINDOWS32**    | O arquivo foi projetado para o Windows de 32 bits.                            |
| **VOS \_ dos \_ WINDOWS16** | O arquivo foi projetado para o Windows de 16 bits em execução com o MS-DOS.        |
| **VOS \_ dos \_ WINDOWS32** | O arquivo foi projetado para o Windows de 32 bits em execução com o MS-DOS.        |
| **VOS \_ NT \_ WINDOWS32**  | O arquivo foi projetado para o Windows de 32 bits.                            |



 

Os valores 0x00002L, 0x00003L, 0x20000L e 0x30000L são reservados.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*Talvez*
</dt> <dd>

Um dos valores a seguir.



| Valor                | Descrição                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ desconhecido**     | O tipo de arquivo é desconhecido.                                                                                                       |
| **\_aplicativo VFT**         | O arquivo contém um aplicativo.                                                                                               |
| **\_dll VFT**         | O arquivo contém uma DLL (biblioteca de vínculo dinâmico).                                                                                 |
| **VFT \_ drv**         | O arquivo contém um driver de dispositivo. Se o *filetype* for **VFT \_ drv**, o *subtipo* conterá uma descrição mais específica do driver. |
| **\_fonte VFT**        | O arquivo contém uma fonte. Se *filetype* for VFT \_ fonte, *subtipo* conterá uma descrição mais específica da fonte.               |
| **VFT \_ vxd**         | O arquivo contém um dispositivo virtual.                                                                                             |
| **\_lib VFT static \_** | O arquivo contém uma biblioteca de vínculo estático.                                                                                        |



 

Todos os outros valores são reservados para uso pela Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*subtipo*
</dt> <dd>

Informações adicionais sobre o tipo de arquivo.

Se *filetype* especificar **VFT \_ drv**, esse parâmetro poderá ser um dos valores a seguir.



| Valor                             | Descrição                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ desconhecido**                 | O tipo de driver é desconhecido.                   |
| **\_Comm VFT2 drv \_**               | O arquivo contém um driver de comunicação.    |
| **\_Impressora VFT2 drv \_**            | O arquivo contém um driver de impressora.           |
| **\_Teclado VFT2 drv \_**           | O arquivo contém um driver de teclado.          |
| **\_Linguagem VFT2 drv \_**           | O arquivo contém um driver de idioma.          |
| **Exibição de VFT2 \_ drv \_**            | O arquivo contém um driver de vídeo.           |
| **\_Mouse VFT2 drv \_**              | O arquivo contém um driver de mouse.             |
| **\_Rede VFT2 drv \_**            | O arquivo contém um driver de rede.           |
| **\_Sistema VFT2 drv \_**             | O arquivo contém um driver de sistema.            |
| **VFT2 \_ drv \_ instalável**        | O arquivo contém um driver instalável.      |
| **\_Som VFT2 drv \_**              | O arquivo contém um driver de som.             |
| **\_Impressora com \_ versão VFT2 \_ drv** | O arquivo contém um driver de impressora com versão. |



 

Se *filetype* especificar **a \_ fonte VFT**, esse parâmetro poderá ser um dos valores a seguir.



| Valor                    | Descrição                    |
|--------------------------|--------------------------------|
| **VFT2 \_ desconhecido**        | O tipo de fonte é desconhecido.          |
| **\_Rasterização de fonte VFT2 \_**   | O arquivo contém uma fonte de varredura.   |
| **\_Vetor de fonte VFT2 \_**   | O arquivo contém uma fonte de vetor.   |
| **Fonte de VFT2 \_ \_ TrueType** | O arquivo contém uma fonte TrueType. |



 

Se *filetype* especificar VFT \_ vxd, esse parâmetro deverá ser o identificador de dispositivo virtual incluído no bloco de controle de dispositivo virtual.

Todos os valores de *subtipo* não listados aqui são reservados para uso pela Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Um dos códigos de idioma a seguir.



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
| 0x0414 | Norueguês? Bokmal  | 0x100C | Francês suíço              |
| 0x0810 | Italiano suíço       | 0x0816 | Português (Portugal)     |
| 0x0813 | Holandês belga       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Norueguês? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Um dos seguintes identificadores de conjunto de caracteres.



| Decimal | Hexadecimal | Conjunto de caracteres              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII de 7 bits                |
| 932     | 03A4        | Japão (Shift? JIS X-0208) |
| 949     | 03B5        | Coreia (Shift? KS 5601)   |
| 950     | 03B6        | Taiwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latim-2 (Europa Oriental) |
| 1251    | 04E3        | Cirílico                   |
| 1252    | 04E4        | Multilíngüe               |
| 1253    | 04E5        | Grego                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Hebraico                     |
| 1256    | 04E8        | Árabe                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nome da cadeia de caracteres*
</dt> <dd>

Um dos nomes predefinidos a seguir.



| Nome                 | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Comentários**         | Informações adicionais que devem ser exibidas para fins de diagnóstico.                                                                                                                                                                                                                                    |
| **CompanyName**      | Empresa que produziu o arquivo? por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc." Essa cadeia de caracteres é necessária.                                                                                                                                                                   |
| **FileDescription**  | Descrição do arquivo a ser apresentado aos usuários. Essa cadeia de caracteres pode ser exibida em uma caixa de listagem quando o usuário estiver escolhendo os arquivos a serem instalados? por exemplo, "driver de teclado para AT-Style teclados". Essa cadeia de caracteres é necessária.                                                                                            |
| **FileVersion**      | Número de versão do arquivo? por exemplo, "3,10" ou "5,00. RC2". Essa cadeia de caracteres é necessária.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno do arquivo, se houver um? por exemplo, um nome de módulo se o arquivo for uma biblioteca de vínculo dinâmico. Se o arquivo não tiver um nome interno, essa cadeia de caracteres deverá ser o nome de arquivo original, sem extensão. Essa cadeia de caracteres é necessária.                                                                       |
| **LegalCopyright**   | Avisos de direitos autorais que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais e assim por diante. Essa cadeia de caracteres é opcional.                                                                                                                                             |
| **LegalTrademarks**  | Marcas registradas e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante. Essa cadeia de caracteres é opcional.                                                                                                                        |
| **OriginalFilename** | Nome original do arquivo, sem incluir um caminho. Essas informações permitem que um aplicativo determine se um arquivo foi renomeado por um usuário. O formato do nome depende do sistema de arquivos para o qual o arquivo foi criado. Essa cadeia de caracteres é necessária.                                                 |
| **PrivateBuild**     | Informações sobre uma versão particular do arquivo? por exemplo, "compilado por TESTER1 em \\ TESTBED". Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ PRIVATEBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz.                                                                                   |
| **ProductName**      | Nome do produto com o qual o arquivo é distribuído. Essa cadeia de caracteres é necessária.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versão do produto com a qual o arquivo é distribuído? por exemplo, "3,10" ou "5,00. RC2". Essa cadeia de caracteres é necessária.                                                                                                                                                                                       |
| **SpecialBuild**     | Texto que indica como esta versão do arquivo difere da versão padrão? por exemplo, "compilação particular para resolução de TESTER1 problemas de mouse em M250 e computadores M250E". Essa cadeia de caracteres deve estar presente somente se o **vs \_ FF \_ SPECIALBUILD** for especificado no parâmetro *FILEFLAGS* do bloco raiz. |



 

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define um recurso **VERSIONINFO** :

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando informações de versão](./using-version-information.md)
</dt> <dt>

[Informações sobre versão](./version-information.md)
</dt> </dl>

 

 