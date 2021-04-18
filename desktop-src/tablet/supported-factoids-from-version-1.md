---
description: A plataforma do Tablet PC dá suporte a várias que são usadas para aumentar a precisão do reconhecimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factos com suporte da versão 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782210"
---
# <a name="supported-factoids-from-version-1"></a>Factos com suporte da versão 1

\[Observe que a seguinte descrição das opções com suporte na versão 1 do SDK (Software Development Kit) do Microsoft Windows XP Tablet PC Edition ainda é suportada por reconhecedores, mas é recomendável que todo o novo desenvolvimento (para os reconhecedores do script Latin) Use os valores definidos na enumeração [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]

A plataforma do Tablet PC dá suporte a várias que são usadas para aumentar a precisão do reconhecimento. Ao usar os factos, é importante que a entrada esperada corresponda exatamente à definição do factor. Se a entrada não corresponder à definição do factor, a precisão do reconhecimento será prejudicada. Por exemplo, se o factor de **número** for definido e o usuário inserir letras, a precisão de reconhecimento de letras será ruim.

Determinados factos, como **email** e **dígito**, são quase idênticos entre os idiomas. Outros factos, como **telefone** e **PostalCode**, variam por idioma. Examine o formato de cada factor para o idioma que você está usando. Uma lista de formatos para cada factor em cada idioma pode ser encontrada nas tabelas nos tópicos que seguem este tópico.

> [!Note]  
> Há uma distinção sutil, mas importante, entre os factos para idiomas ocidentais e as para idiomas do leste asiático. Os factos para idiomas ocidentais são implementados usando expressões que descrevem o resultado desejado. O reconhecedor é então polarizado para produzir resultados que correspondam a essa expressão. As opções para idiomas do Leste Asiático são implementadas especificando um intervalo aceitável de caracteres Unicode. Por exemplo, o facto de **Data** para idiomas do leste asiático aceita somente caracteres Unicode em um determinado intervalo.

 

Os factos para os idiomas ocidentais incluem para inglês (Reino Unido), inglês (Estados Unidos), francês, alemão e espanhol. Os factos para os idiomas do leste asiático incluem o factos para chinês (simplificado), chinês (tradicional), japonês e coreano.

As seções a seguir mostram os formatos com suporte para cada factor em cada idioma:

-   [Factos comuns entre linguagens](factoids-common-across-languages.md)
-   [Factos para idiomas ocidentais](factoids-for-western-languages.md)
-   [Factos para idiomas do leste asiático](factoids-for-east-asian-languages.md)

Se você esperar uma entrada diferente dos formatos listados nas tabelas nessas seções, não use um factor. Além disso, os factos são incorporados ao reconhecedor para cada idioma. Você não pode usar os factos de um idioma com um reconhecedor de outro idioma. Por exemplo, você não pode usar o botão de **telefone** francês com um reconhecedor japonês.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes do factor**](factoid-constants.md)
</dt> <dt>

[Classe Microsoft. Ink. Factoname](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
