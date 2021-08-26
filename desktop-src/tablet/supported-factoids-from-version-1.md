---
description: A Plataforma de Tablet PC dá suporte a vários factoids que são usados para aumentar a precisão do reconhecimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids com suporte da versão 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934346"
---
# <a name="supported-factoids-from-version-1"></a>Factoids com suporte da versão 1

\[Observe que a descrição a seguir dos factoids com suporte na versão 1 do SDK (Software Development Kit) do Microsoft Windows TABLET PC Edition (SDK) ainda tem suporte dos reconhecedores, mas é recomendável que todos os novos desenvolvimentos (para reconhecedores de script latino) usem os valores definidos na enumeração [InputScope.](/windows/win32/api/inputscope/ne-inputscope-inputscope)\]

A Plataforma de Tablet PC dá suporte a vários factoids que são usados para aumentar a precisão do reconhecimento. Ao usar factoids, é importante que a entrada esperada corresponder exatamente à definição do factoid. Se a entrada não corresponder à definição do factoid, a precisão do reconhecimento sofrerá. Por exemplo, se o factoid **Number** estiver definido e o usuário inserir letras, a precisão de reconhecimento das letras será ruim.

Determinados factoids, como **Email e** **Dígito,** são quase idênticos entre idiomas. Outros factoids, como **Telefone e** **PostalCode,** variam de acordo com o idioma. Examine o formato de cada factoid para o idioma que você está usando. Uma lista de formatos para cada factoid em cada idioma pode ser encontrada nas tabelas nos tópicos a seguir neste tópico.

> [!Note]  
> Há uma distinção sutil, mas importante entre factoids para idiomas ocidental e factoids para idiomas do Leste da Ásia. Factoids para linguagens ocidental são implementados usando expressões que descrevem o resultado desejado. Em seguida, o reconhecedor é polarizado para produzir resultados que corresponderem a essa expressão. Factoids para idiomas do Leste da Ásia são implementados especificando um intervalo aceitável de caracteres Unicode. Por exemplo, o **factoid Date** para idiomas do Leste da Ásia aceita apenas caracteres Unicode dentro de um determinado intervalo.

 

Factoids para idiomas do oeste incluem factoids para inglês (Reino Unido), inglês (Estados Unidos), francês, alemão e espanhol. Factoids para idiomas do Leste da Ásia incluem factoids para chinês (simplificado), chinês (tradicional), japonês e coreano.

As seções a seguir mostram os formatos com suporte para cada factoid em cada idioma:

-   [Factoids comuns entre linguagens](factoids-common-across-languages.md)
-   [Factoids para idiomas do oeste](factoids-for-western-languages.md)
-   [Factoids para idiomas do Leste da Ásia](factoids-for-east-asian-languages.md)

Se você espera uma entrada diferente dos formatos listados nas tabelas nessas seções, não use um factoid. Além disso, factoids são integrados ao reconhecedor para cada idioma. Você não pode usar factoids de um idioma com um reconhecedor de outro idioma. Por exemplo, você não pode usar o factoid **telefone** francês com um reconhecedor japonês.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes factoid**](factoid-constants.md)
</dt> <dt>

[Classe Microsoft.Ink.Factoid](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
