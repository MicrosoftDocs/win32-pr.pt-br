---
title: Instrução VarFileInfo BLOCK
description: Descreve a forma do bloco de informações da variável.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menus de instrução VarFileInfo BLOCK e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006692"
---
# <a name="varfileinfo-block-statement"></a>Instrução VarFileInfo BLOCK

Define um bloco de informações de variável.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Um dos identificadores de idioma especificados na seção comentários.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Um dos identificadores de conjunto de caracteres especificados na seção comentários.

</dd> </dl>

## <a name="remarks"></a>Comentários

Mais de um par de identificadores pode ser fornecido, mas cada par deve ser separado do par anterior com uma vírgula.

O parâmetro *LangID* especifica um dos seguintes códigos de idioma.



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



 

O parâmetro *charsetID* especifica um dos seguintes identificadores de conjunto de caracteres:



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



 

 

 




