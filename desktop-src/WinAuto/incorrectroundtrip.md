---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644727"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Texto

Chamar accNavigate((Clique em Enooze para ser lembrado novamente em:), 1, NAVDIR \_ NEXT), em seguida, accNavigate((Open), 2, NAVDIR PREVIOUS), deve ter retornado Click Snooze para ser lembrado novamente em:(ChildId=1), mas retornou Clique em Esnooze para ser lembrado novamente \_ em:

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

usar [**accNavigate para**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) percorrer a árvore de elementos do destino de verificação não retorna o mesmo elemento inicial quando a direção da travessia é invertida.

![exemplo de uma implementação de msaa inválida que causou navegação de ida e volta incorreta](images/accchecker-invalid-round-trip.png)

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque a travessia de elementos pode ser imprevisível e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




