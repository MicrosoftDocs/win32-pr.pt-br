---
description: Os caracteres definidos pelo usuário final (EUDC) em conjuntos de caracteres de dois bytes (DBCS) e caracteres de área de uso particular (PUA) em Unicode são caracteres personalizados.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caracteres da área de uso privado e definido pelo usuário final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297277"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caracteres da área de uso privado e definido pelo usuário final

Os caracteres definidos pelo usuário final (EUDC) em [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) (DBCS) e caracteres de área de uso particular (pua) em [Unicode](unicode.md) são caracteres personalizados. Eles podem ser definidos e implementados por um usuário final ou por outra parte, como um fabricante de equipamento, um grupo de usuários, um corpo governamental ou uma empresa de design de fontes. Seu uso permite que os usuários formem nomes e outras palavras usando caracteres que não estão disponíveis em fontes de tela e de impressora padrão.

Os caracteres EUDC e PUA podem ser atribuídos de forma diferente, ou não atribuídos, em computadores diferentes. Algumas páginas de código têm extensões que reutilizam o intervalo EUDC, e essas extensões podem entrar em conflito entre si. Em outros casos, um fabricante pode fornecer um conjunto personalizado de caracteres em um desses intervalos. Além disso, os grupos de usuários podem tentar fornecer caracteres adicionais no PUA. Diferentes combinações desses casos podem causar conflitos. Ao criar aplicativos que dependem de caracteres EUDC ou PUA, você deve ter em mente as interpretações conflitantes de um ponto de código individual.

Os tópicos a seguir discutem as fontes que dão suporte a EUDCs e acesso e gerenciamento para estes caracteres:

-   [Fontes e conjuntos de caracteres](character-sets-and-fonts.md)
-   [Entradas do registro EUDC](eudc-registry-entries.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Unicode e conjuntos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



