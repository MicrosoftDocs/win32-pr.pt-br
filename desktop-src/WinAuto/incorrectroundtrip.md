---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160184"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texto

Chame para accNavigate (clique em adiar para ser lembrado novamente em:), 1, NAVDIR \_ Next), em seguida, accNavigate ((Open), 2, NAVDIR \_ Previous), deve ter retornado clique em adiar para ser lembrado novamente em: (childID = 1), mas retornado clique em adiar para ser lembrado novamente em:

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

usar [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para atravessar a árvore de elementos do destino de verificação não retorna o mesmo elemento inicial quando a direção de passagem é invertida.

![exemplo de uma implementação de MSAA inválida que causou navegação de ida e volta incorreta](images/accchecker-invalid-round-trip.png)

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a passagem de elementos pode ser irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




