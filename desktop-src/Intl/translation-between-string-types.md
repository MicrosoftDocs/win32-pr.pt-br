---
description: As funções listadas na tabela a seguir convertem cadeias de caracteres de um tipo de cadeia de caracteres para outro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversão entre tipos de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b62ae39307e92c203441ea8ddb9dc61b394a02622e3c86a8949b59539588585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631916"
---
# <a name="translation-between-string-types"></a>Conversão entre tipos de cadeia de caracteres

As funções listadas na tabela a seguir convertem cadeias de caracteres de um tipo de cadeia de caracteres para outro.



| Função                                           | Descrição                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Traduz uma cadeia de caracteres para outra.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Mapas uma cadeia de caracteres por localidade.                      |
| [**Tounicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Traduz um código de chave virtual em um caractere Unicode. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Mapas uma cadeia de caracteres multibyte para uma cadeia de caracteres Unicode.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Mapas uma cadeia de caracteres Unicode para uma cadeia de caracteres multibyte.            |



 

As funções [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) são particularmente úteis para aplicativos que dão suporte a vários tipos de cadeia de caracteres. ANSI C também define as funções de conversão **wcstombs** e **mbstowcs**, mas elas só podem converter de e para o conjunto de caracteres com suporte na biblioteca C padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
