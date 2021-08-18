---
title: Recurso VERSIONINFO
description: Define um recurso de informações de versão. O recurso contém essas informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original. O recurso destina-se a ser usado com as funções informações de versão.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menus de recurso VERSIONINFO e outros recursos
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6708b4fefc564685a9989140e5f07dd20714e8bbcb60c53710f43cbfee4aa7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971865"
---
# <a name="versioninfo-resource"></a>Recurso VERSIONINFO

Define um recurso de informações de versão. O recurso contém essas informações sobre o arquivo como seu número de versão, seu sistema operacional pretendido e seu nome de arquivo original. O recurso destina-se a ser usado com as funções [informações de](./version-information.md) versão.

Há duas maneiras de formatar uma **instrução VERSIONINFO:**

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

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*Versionid*
</dt> <dd>

Identificador de recurso de informações de versão. Esse valor deve ser 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*informações fixas*
</dt> <dd>

Informações de versão, como a versão do arquivo e o sistema operacional pretendido. Esse parâmetro consiste nas instruções a seguir.



| Instrução                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versão do FILEVERSION**          | Número de versão binária para o arquivo. A *versão* consiste em dois inteiros de 32 bits, definidos por quatro inteiros de 16 bits. Por exemplo, "FILEVERSION 3,10,0,61" é convertido em duas palavras duplas: 0x0003000a e 0x0000003d, nessa ordem. Portanto, se *a* versão for definida pelos valores **DWORD** *dw1* e *dw2*, ela precisará aparecer na instrução **FILEVERSION** da seguinte forma: `HIWORD(dw1)` , , , `LOWORD(dw1)` `HIWORD(dw2)` `LOWORD(dw2)` . |
| **Versão do PRODUCTVERSION**       | Número de versão binária para o produto com o qual o arquivo é distribuído. O *parâmetro* version é dois inteiros de 32 bits, definidos por quatro inteiros de 16 bits. Para obter mais informações sobre *a versão*, consulte a **descrição FILEVERSION.**                                                                                                                                                                                                           |
| **FileFLAGSMASK** *fileflagsmask* | Indica quais bits na instrução **FILEFLAGS são** válidos. Para 16 bits Windows, esse valor é 0x3f.                                                                                                                                                                                                                                                                                                                                          |
| **FileFLAGS** *fileflags*         | Atributos do arquivo.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FileOS** *fileos*               | Sistema operacional para o qual esse arquivo foi projetado. O *parâmetro fileos* pode ser um dos valores do sistema operacional determinados na seção Comentários.                                                                                                                                                                                                                                                                                               |
| **Tipo de arquivo FILETYPE**            | Tipo geral de arquivo. O *parâmetro filetype* pode ser um dos valores de tipo de arquivo listados na seção Comentários.                                                                                                                                                                                                                                                                                                                                |
| **Subtipo FILESUBTYPE**          | Função do arquivo. O *parâmetro de subtipo* é zero, a menos que o parâmetro *filetype* na instrução **FILETYPE** seja VFT \_ DRV, VFT \_ FONT ou VFT \_ VXD. Para ver uma lista de valores de subtipo de arquivo, consulte a seção Comentários.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*instrução block*
</dt> <dd>

Especifica um ou mais blocos de informações de versão. Um bloco pode conter informações de cadeia de caracteres ou informações de variável. Para obter mais informações, consulte [**Bloco StringFileInfo ou**](stringfileinfo-block.md) [**Bloco VarFileInfo**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar as constantes especificadas com a instrução **VERSIONINFO,** você deve incluir o arquivo de título Winver.h ou Windows.h no arquivo de definição de recurso.

A lista a seguir descreve os parâmetros usados na **instrução VERSIONINFO:**

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*Fileflags*
</dt> <dd>

Uma combinação dos valores a seguir.



| Valor                      | Descrição                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DEPURAÇÃO DO VS \_ \_ FF**          | O arquivo contém informações de depuração ou é compilado com recursos de depuração habilitados.                                                                                                                                                                                         |
| **VS \_ FF \_ PATCHED**        | O arquivo foi modificado e não é idêntico ao arquivo de envio original do mesmo número de versão.                                                                                                                                                                       |
| **PRÉ-LANÇAMENTO DO VS \_ FF \_**     | O arquivo é uma versão de desenvolvimento, não um produto lançado comercialmente.                                                                                                                                                                                                         |
| **PRIVATEBUILD do VS \_ FF \_**   | O arquivo não foi criado usando procedimentos de versão padrão. Se esse valor for dado, o [**bloco StringFileInfo deverá**](stringfileinfo-block.md) conter uma **cadeia de caracteres PrivateBuild.**                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | O arquivo foi criado pela empresa original usando procedimentos de versão padrão, mas é uma variação do arquivo padrão do mesmo número de versão. Se esse valor for dado, o bloco [ **StringFileInfo**](stringfileinfo-block.md) deverá conter uma cadeia de caracteres **SpecialBuild.** |
| **VS \_ FFI \_ FILEFLAGSMASK** | Uma combinação de todos os valores anteriores.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

Um dos valores a seguir.



| Valor                   | Descrição                                                      |
|-------------------------|------------------------------------------------------------------|
| **OPERAÇÃO \_ DESCONHECIDA**        | O sistema operacional para o qual o arquivo foi projetado é desconhecido. |
| **VOS \_ DOS**            | O arquivo foi projetado para o MS-DOS.                                    |
| **OPERAÇÃO \_ NT**             | O arquivo foi projetado para 32 bits Windows.                            |
| **OPERAÇÃO \_ \_ WINDOWS16**    | O arquivo foi projetado para 16 bits Windows.                            |
| **OPERAÇÃO \_ \_ WINDOWS32**    | O arquivo foi projetado para 32 bits Windows.                            |
| **OPERAÇÃO \_ DOS \_ WINDOWS16** | O arquivo foi projetado para 16 bits Windows em execução com o MS-DOS.        |
| **OPERAÇÃO \_ DOS \_ WINDOWS32** | O arquivo foi projetado para 32 bits Windows em execução com o MS-DOS.        |
| **OPERAÇÃO \_ NT \_ WINDOWS32**  | O arquivo foi projetado para 32 bits Windows.                            |



 

Os valores 0x00002L, 0x00003L, 0x20000L e 0x30000L são reservados.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*Filetype*
</dt> <dd>

Um dos valores a seguir.



| Valor                | Descrição                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ UNKNOWN**     | O tipo de arquivo é desconhecido.                                                                                                       |
| **APLICATIVO \_ VFT**         | O arquivo contém um aplicativo.                                                                                               |
| **DLL \_ do VFT**         | O arquivo contém uma DLL (biblioteca de vínculo dinâmico).                                                                                 |
| **DRV do VFT \_**         | O arquivo contém um driver de dispositivo. Se *filetype* for **\_ DRV da VFT,** *o subtipo* conterá uma descrição mais específica do driver. |
| **FONTE \_ VFT**        | O arquivo contém uma fonte. Se *filetype* for FONT \_ VFT, o *subtipo* conterá uma descrição mais específica da fonte.               |
| **VFT \_ VXD**         | O arquivo contém um dispositivo virtual.                                                                                             |
| **BIBLIOTECA ESTÁTICA do VFT \_ \_** | O arquivo contém uma biblioteca de vínculo estático.                                                                                        |



 

Todos os outros valores são reservados para uso pela Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*Subtipo*
</dt> <dd>

Informações adicionais sobre o tipo de arquivo.

Se *filetype* especificar **\_ DRV da VFT,** esse parâmetro poderá ser um dos valores a seguir.



| Valor                             | Descrição                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ UNKNOWN**                 | O tipo de driver é desconhecido.                   |
| **VFT2 \_ DRV \_ COMM**               | O arquivo contém um driver de comunicação.    |
| **IMPRESSORA DRV VFT2 \_ \_**            | O arquivo contém um driver de impressora.           |
| **TECLADO DRV VFT2 \_ \_**           | O arquivo contém um driver de teclado.          |
| **LINGUAGEM DRV VFT2 \_ \_**           | O arquivo contém um driver de idioma.          |
| **VFT2 \_ DRV \_ DISPLAY**            | O arquivo contém um driver de exibição.           |
| **VFT2 \_ DRV \_ MOUSE**              | O arquivo contém um driver do mouse.             |
| **REDE DE DRV VFT2 \_ \_**            | O arquivo contém um driver de rede.           |
| **SISTEMA DRV VFT2 \_ \_**             | O arquivo contém um driver do sistema.            |
| **VFT2 \_ DRV \_ INSTALLABLE**        | O arquivo contém um driver instalável.      |
| **SOM DRV VFT2 \_ \_**              | O arquivo contém um driver de som.             |
| **IMPRESSORA COM \_ VERSÃO DE DRV VFT2 \_ \_** | O arquivo contém um driver de impressora com versão. |



 

Se *filetype* especificar **FONT VFT \_**, esse parâmetro poderá ser um dos valores a seguir.



| Valor                    | Descrição                    |
|--------------------------|--------------------------------|
| **VFT2 \_ UNKNOWN**        | O tipo de fonte é desconhecido.          |
| **RASTER DE FONTE VFT2 \_ \_**   | O arquivo contém uma fonte raster.   |
| **VETOR DE FONTE VFT2 \_ \_**   | O arquivo contém uma fonte de vetor.   |
| **VFT2 \_ FONT \_ TRUETYPE** | O arquivo contém uma fonte TrueType. |



 

Se *filetype* especificar \_ VFT VXD, esse parâmetro deverá ser o identificador de dispositivo virtual incluído no bloco de controle de dispositivo virtual.

Todos *os valores de* subtipo não listados aqui são reservados para uso pela Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

Um dos códigos de idioma a seguir.



| Código   | Linguagem            | Código   | Linguagem                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Árabe              | 0x0415 | Polonês                    |
| 0x0402 | Búlgaro           | 0x0416 | Português (Brasil)       |
| 0x0403 | Catalão             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinês tradicional | 0x0418 | Romeno                  |
| 0x0405 | Tcheco               | 0x0419 | Russo                   |
| 0x0406 | Dinamarquês              | 0x041A | Croato-Serbian (latino)    |
| 0x0407 | Alemão              | 0x041B | Eslovaco                    |
| 0x0408 | Grego               | 0x041C | Albanês                  |
| 0x0409 | Inglês dos EUA        | 0x041D | Sueco                   |
| 0x040A | Castiliano espanhol   | 0x041e | Tailandês                      |
| 0x040B | Finlandês             | 0x041F | Turco                   |
| 0x040C | Francês              | 0x0420 | Urdu                      |
| 0x040D | Hebraico              | 0x0421 | Bahasa                    |
| 0x040E | Húngaro           | 0x0804 | Chinês simplificado        |
| 0x040F | Islandês           | 0x0807 | Alemão alemão              |
| 0x0410 | Italiano             | 0x0809 | Reino Unido Inglês              |
| 0x0411 | Japonês            | 0x080A | Espanhol (México)          |
| 0x0412 | Coreano              | 0x080C | Francês francês francês            |
| 0x0413 | Holandês               | 0x0C0C | Francês do Canadá           |
| 0x0414 | Norueguês? Bokmal  | 0x100C | Francês francês              |
| 0x0810 | Italiano italiano       | 0x0816 | Português (Portugal)     |
| 0x0813 | Holandês holandês       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Norueguês? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Um dos seguintes identificadores de conjunto de caracteres.



| Decimal | Hexadecimal | Conjunto de caracteres              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII de 7 bits                |
| 932     | 03A4        | Japão (Shift ? JIS X-0208) |
| 949     | 03B5        | Coreia do Sul (Shift ? KSC 5601)   |
| 950     | 03B6        | Taiwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latin-2 (Leste da Europa) |
| 1251    | 04E3        | Cirílico                   |
| 1252    | 04E4        | Multilingue               |
| 1253    | 04E5        | Grego                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Hebraico                     |
| 1256    | 04E8        | Árabe                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
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

 

 