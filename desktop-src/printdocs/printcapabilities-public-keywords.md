---
description: Saiba mais sobre os elementos configuráveis do usuário e definições de parâmetros que podem ser aplicáveis a um documento de PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palavras-chave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407089"
---
# <a name="printcapabilities-public-keywords"></a>Palavras-chave públicas de PrintCapabilities

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A seção a seguir especifica os elementos configuráveis pelo usuário e as definições de parâmetro que podem ser aplicáveis a um documento de PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Uso de elementos configuráveis pelo usuário

Os elementos configuráveis pelo usuário representam as palavras-chave públicas do esquema de impressão que podem aparecer em um documento de PrintCapabilities ou em um PrintTicket. Eles têm a finalidade de representar os atributos de dispositivo configuráveis com suporte em um dispositivo específico ou comunicar a intenção de configuração de impressão por um aplicativo ou usuário.

Elementos configuráveis pelo usuário podem referenciar elementos de referência de parâmetro. Para obter mais informações, consulte a seção [elementos de referência de parâmetro](parameter-reference-elements.md) .

## <a name="parameter-definitions-usage"></a>Uso de definições de parâmetro

As definições de parâmetros assumem a forma de tipos de elementos ParameterDef em um documento de recursos de impressão. Os tipos de elementos ParameterDef são inicializados em um PrintTicket usando o tipo de elemento ParameterInit. O valor do parâmetro será especificado usando o elemento ParameterInit. Uma palavra-chave configurável pelo usuário pode fazer referência a uma definição de parâmetro usando o tipo de elemento ParameterRef. Para obter mais informações, consulte a seção [construções de parâmetro](parameter-constructs.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



