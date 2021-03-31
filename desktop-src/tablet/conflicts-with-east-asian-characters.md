---
description: Alguns gestos de aplicativo podem entrar em conflito com caracteres do leste asiático ou combinações de caracteres do leste asiático.
ms.assetid: 56ff773f-ef95-47f8-ba04-2593330867ee
title: Conflitos com East-Asian caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb12b9fab1389395b249f35da3dc5ffbfc91af83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089860"
---
# <a name="conflicts-with-east-asian-characters"></a>Conflitos com East-Asian caracteres

Alguns *gestos de aplicativo* podem entrar em conflito com caracteres do leste asiático ou combinações de caracteres do leste asiático. A tabela a seguir lista os possíveis conflitos entre os gestos do aplicativo e os caracteres em aplicativos que têm entrada de caracteres específica do leste asiático.



| Gesto                 | Chinês (Simplificado) | Chinês (Tradicional) | Japonês     | Coreano       |
|-------------------------|----------------------|-----------------------|--------------|--------------|
| Down<br/>         | X<br/>         | X<br/>          | X<br/> | X<br/> |
| Direita<br/>        | X<br/>         | X<br/>          | X<br/> | X<br/> |
| DownRight<br/>    | -<br/>         | X<br/>          | -<br/> | X<br/> |
| RightDown<br/>    | -<br/>         | -<br/>          | X<br/> | X<br/> |
| Circle<br/>       | -<br/>         | -<br/>          | -<br/> | X<br/> |
| ChevronRight<br/> | -<br/>         | -<br/>          | -<br/> | X<br/> |



 

A Microsoft continua comprometida com o desenvolvimento de *gestos*. A Microsoft reconhece que, na criação de aplicativos, os ISVs (fornecedores independentes de software) precisam saber quais ações serão mapeadas para gestos. [Glifos não implementados](unimplemented-glyphs.md) lista um conjunto de ações de caneta que a Microsoft planeja mapear para gestos, bem como gestos que estão sendo reservados para ações. Essas informações são fornecidas para que você saiba quais ações e gestos serão fornecidos no futuro.

Além de usar gestos fornecidos no Microsoft Windows XP Tablet PC Edition, os aplicativos são livres para criar seus próprios gestos. Esses gestos podem ser reconhecidos por um *reconhecedor de gestos da Microsoft* criado pelo desenvolvedor de aplicativos. Se você planeja implementar qualquer um dos seus próprios gestos, consulte [glifos não implementados](unimplemented-glyphs.md) para evitar sobreposição com gestos que a Microsoft planeja implementar.

 

 




