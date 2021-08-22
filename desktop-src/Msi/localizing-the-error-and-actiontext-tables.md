---
description: O Microsoft Windows SDK (Software Development Kit) inclui cadeias de caracteres de recursos localizadas, tabelas de erro localizadas e tabelas ActionText localizadas para os idiomas listados na tabela a seguir.
ms.assetid: 2e3a6e73-5b06-452d-9f87-18eb6914b961
title: Localizando as tabelas Error e ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1839141b80afd1d28aa9e9317da10d79aea41232f9e7ebde0db7971d22f5141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629461"
---
# <a name="localizing-the-error-and-actiontext-tables"></a>Localizando as tabelas Error e ActionText

O Microsoft Windows Software Development Kit (SDK) inclui cadeias de caracteres de recursos localizadas, tabelas de erro localizadas [e](error-table.md)tabelas [ActionText](actiontext-table.md) localizadas para os idiomas listados na tabela a seguir. Os LANGIDs marcados com asteriscos indicam que as cadeias de caracteres de recurso são armazenadas como o idioma base e, portanto, podem ser usadas com todos os dialetos desse idioma.

Você pode importar as tabelas Error e ActionText localizadas para seu banco de dados usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).



| LANGID (decimal) | LANGID (hexadecimal) | Página de código ASCII | Abreviação | Idioma                      | Language-Culture |
|------------------|----------------------|-----------------|--------------|-------------------------------|------------------|
| 1025\*           | 0x401                | 1256            | Ara          | Árabe - Arábia Saudita         | ar-SA            |
| 1027             | 0x403                | 1252            | Gato          | Catalão                       | ca-ES            |
| 1028\*           | 0x404                | 950             | CHT          | Chinês – Taiwan              | zh-TW            |
| 2052             | 0x804                | 936             | CHS          | Chinês – China               | zh-CN            |
| 1029             | 0x405                | 1250            | CSY          | Tcheco – República Tcheca        | cs-CZ            |
| 1030             | 0x406                | 1252            | DAN          | Dinamarquês -Deção               | da-DK            |
| 1031\*           | 0x407                | 1252            | DEU          | Alemão - Alemanha              | de-DE            |
| 1032             | 0x408                | 1253            | ELL          | Grego – Glândia                | el-GR            |
| 1033\*           | 0x409                | 1252            | ENU          | Portuguese - Brazil       | pt-BR            |
| 3082\*           | 0xC0A                | 1252            | ESN          | Espanhol – Classificação Moderna – Espanha | es-ES            |
| 1061             | 0x425                | 1257            | ETI          | Estoniano                      | et-EE            |
| 1035             | 0x40B                | 1252            | FIN          | Finlândia – Finlândia             | fi-FI            |
| 1036\*           | 0x40C                | 1252            | FRA          | Francês - França               | fr-FR            |
| 1037             | 0x40D                | 1255            | Heb          | Hebraico – Hebraico               | he-IL            |
| 1038             | 0x40E                | 1250            | HUN          | Húngaro-Hungria           | hu-HU            |
| 1040\*           | 0x410                | 1252            | ITA          | Italiano - Itália               | it-IT            |
| 1041             | 0x411                | 932             | JPN          | Japonês - Japão              | jp-JP            |
| 1042             | 0x412                | 949             | KOR          | Coreano - Coreia do Sul                | Ko-KO            |
| 1063             | 0x427                | 1257            | LTH          | Lituano                    | lt-LT            |
| 1062             | 0x426                | 1257            | LVI          | Letão                       | lv-LV            |
| 1043\*           | 0x413                | 1252            | NLD          | Holandês - Países Baixos           | nl-NL            |
| 1044\*           | 0x414                | 1252            | NOR          | Norueguês (bokmål) – Noruega    | nb-NO            |
| 1045             | 0x415                | 1250            | PLK          | Polonês – Polônia                | pl-PL            |
| 1046             | 0x416                | 1252            | PTB          | Português - Brasil           | pt-BR            |
| 2070             | 0x816                | 1252            | PTG          | Português - Portugal         | pt-PT            |
| 1048             | 0x418                | 1250            | ROM          | Romeno-Romênia            | ro-RO            |
| 1049             | 0x419                | 1251            | RUS          | Russo – Rússia              | ru-RU            |
| 1.050             | 0x41A                | 1250            | HRV          | Croata-Croácia            | hr-HR            |
| 1051             | 0x41B                | 1250            | Celeste          | Eslovaco-Eslováquia             | sk-SK            |
| 1053\*           | 0x41D                | 1252            | SVE          | Sueco-Suécia              | sv-SE            |
| 1054             | 0x41E                | 874             | THA          | Tailandês-Tailândia               | th-TH            |
| 1055             | 0x41F                | 1254            | TRK          | Turco-Turquia              | tr-TR            |
| 1060             | 0x424                | 1250            | SLV          | Esloveno-Eslovênia          | sl-SI            |
| 1066             | 0x42A                | 1258            | VIT          | Vietnamita-Vietnã         | vi-VN            |
| 1069             | 0x42D                | 1252            | EUQ          | Basco (País Basco)               | eu-ES            |



 

**Windows Vista:** além dos idiomas listados na tabela anterior, os idiomas na tabela a seguir estão disponíveis a partir do Windows Vista.



| LANGid (Decimal) | LANGid (hexadecimal) | Página de código ASCII | Abreviação | Idioma        | Language-Culture |
|------------------|----------------------|-----------------|--------------|-----------------|------------------|
| 1026             | 0x402                | 1251            | BGR          | Búlgaro       | bg-BG            |
| 1058             | 0x422                | 1251            | UKR          | Ucraniano       | uk-UA            |
| 2074             | 0x81A                | 1250            | SRL          | Sérvio (latino) | sr-Latn-CS       |



 

 

 



