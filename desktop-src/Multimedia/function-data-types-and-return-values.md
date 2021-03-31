---
title: Tipos de dados de função e valores de retorno
description: Tipos de dados de função e valores de retorno
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916192"
---
# <a name="function-data-types-and-return-values"></a>Tipos de dados de função e valores de retorno

As funções e macros do AVIFile usam manipuladores de arquivo e fluxo implementados com a tecnologia OLE. O tipo de dados padrão de uma função OLE é **STDAPI**, e a função retorna um valor **HRESULT** (zero para êxito ou erro de outra forma). Se uma função retornar um valor diferente de um **HRESULT**, o tipo do protótipo da função terá uma sintaxe ligeiramente diferente que incorporará o tipo de valor de retorno entre parênteses após "STDAPI \_ ". Por exemplo, uma função que retorna um valor de dados **Long** usa **STDAPI \_ (Long)** na instrução de protótipo.

 

 




