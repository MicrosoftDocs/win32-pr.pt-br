---
title: Invocando o compilador MIDL
description: O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema. Consulte a opção/target para saber mais sobre as opções sugeridas e como gerar código otimizado para uma versão específica.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL do compilador MIDL, invocando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2019
ms.locfileid: "105751454"
---
# <a name="invoking-the-midl-compiler"></a>Invocando o compilador MIDL

O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema. Consulte a opção [**/target**](-target.md) para saber mais sobre as opções sugeridas e como gerar código otimizado para uma versão específica.

Execute o compilador MIDL na linha de comando usando o seguinte comando:

 *<  opções >* de MIDL **filename. idl**

onde *< ***as opções*** >* representam as opções de linha de comando que você deseja usar e filename. idl é o nome do arquivo MIDL a ser compilado.

Uma lista completa dos comutadores e opções do compilador de MIDL está disponível quando você usa o compilador MIDL [**/Help**](-help-.md) e/? comutadores. As opções são organizadas por categorias. Para obter detalhes, consulte a [referência de Command-Line MIDL](midl-command-line-reference.md).

> [!NOTE]
> O novo sinalizador global **$ (otimização de MIDL \_ )** existe no Win32. Mak. Quando um arquivo. idl é compilado usando esse sinalizador, o stub gerado pode utilizar os recursos de RPC mais recentes disponíveis na plataforma especificada e, potencialmente, melhorar o desempenho e a estabilidade do aplicativo. É recomendável que os aplicativos usem esse sinalizador ao usar MIDL.
>
> **MIDL** **$ (otimização de MIDL \_ )** **...**