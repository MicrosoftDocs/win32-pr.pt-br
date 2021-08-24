---
description: Saiba mais sobre elementos configuráveis pelo usuário e definições de parâmetro que podem ser aplicáveis a um documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palavras-chave públicas PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cccfa2cb22d8e784e8d4b82e548b9f4ae9772d1bd216573f5229d00f2f6d633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600616"
---
# <a name="printcapabilities-public-keywords"></a>Palavras-chave públicas PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A seção a seguir especifica elementos configuráveis pelo usuário e definições de parâmetro que podem ser aplicáveis a um documento PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Uso de elementos configuráveis pelo usuário

Elementos configuráveis pelo usuário representam palavras-chave públicas de esquema de impressão que podem aparecer em um documento PrintCapabilities ou em um PrintTicket. Eles destinam-se a representar atributos de dispositivo configuráveis com suporte de um dispositivo específico ou comunicar a intenção de configuração de impressão por um aplicativo ou usuário.

Elementos configuráveis pelo usuário podem referenciar elementos de referência de parâmetro. Para obter mais informações, consulte a seção [Elementos de referência de parâmetro.](parameter-reference-elements.md)

## <a name="parameter-definitions-usage"></a>Uso de definições de parâmetro

As definições de parâmetros assumirão a forma de tipos de elemento ParameterDef em um documento Funcionalidades de Impressão. Os tipos de elemento ParameterDef são inicializados em um PrintTicket usando o tipo de elemento ParameterInit. O valor do parâmetro será especificado usando o elemento ParameterInit. Uma palavra-chave configurável pelo usuário pode referenciar uma definição de parâmetro usando o tipo de elemento ParameterRef. Para obter mais informações, consulte a seção [Constructos de parâmetro.](parameter-constructs.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



