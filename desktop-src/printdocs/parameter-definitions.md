---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definições de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172555"
---
# <a name="parameter-definitions"></a>Definições de parâmetro

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esta seção descreve as definições de parâmetros públicos que podem aparecer em um documento de PrintCapabilities.

Os parâmetros são usados para descrever um intervalo aceitável de valores, em vez de uma enumeração discreta de valores.

## <a name="parameterdef"></a>ParameterDef

Para obter um resumo do tipo de elemento ParameterDef, consulte a seção [ParameterDef](parameterdef.md) .

Para obter mais informações sobre a interação entre elementos ParameterDef e elementos ParameterInit, consulte a seção de [elementos ParameterDef e ParameterInit](./parameterdef-and-parameterinit-elements.md) .

Os elementos ParameterDef definidos nas palavras-chave do esquema de impressão devem ser totalmente definidos em um documento PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Para obter um resumo do tipo de elemento ParameterRef, consulte a seção [ParameterRef](parameterref.md) .

Uma palavra-chave de elemento configurável pelo usuário pode conter uma referência a um parâmetro. Os elementos ParameterRef são especificados como um filho de um elemento ScoredProperty para obter mais informações, consulte a seção [elementos de referência de parâmetro](parameter-reference-elements.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
