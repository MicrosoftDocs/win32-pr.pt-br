---
title: Instrução BLOCK VarFileInfo
description: Descreve a forma do bloco de informações de variável.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menus de instrução BLOCK VarFileInfo e outros recursos
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846966"
---
# <a name="varfileinfo-block-statement"></a>Instrução BLOCK VarFileInfo

Define um bloco de informações de variável.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

Um dos identificadores de idioma especificados na seção Comentários.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Um dos identificadores de conjunto de caracteres especificados na seção Comentários.

</dd> </dl>

## <a name="remarks"></a>Comentários

Mais de um par de identificadores pode ser dado, mas cada par deve ser separado do par anterior com uma vírgula.

O *parâmetro langID* especifica um dos códigos de idioma a seguir.



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
| 0x0414 | Norueguês – Bokmal  | 0x100C | Francês francês              |
| 0x0810 | Italiano italiano       | 0x0816 | Português (Portugal)     |
| 0x0813 | Holandês holandês       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Norueguês – Nynorsk | ?      | ?                         |



 

O *parâmetro charsetID* especifica um dos seguintes identificadores de conjunto de caracteres:



| Identificador | Conjunto de caracteres              |
|------------|----------------------------|
| 0          | ASCII de 7 bits                |
| 932        | Japão (Shift – JIS X-0208) |
| 949        | Coreia do Sul (Shift – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Leste da Europa) |
| 1251       | Cirílico                   |
| 1252       | Multilingue               |
| 1253       | Grego                      |
| 1254       | Turco                    |
| 1255       | Hebraico                     |
| 1256       | Árabe                     |



 

 

 




