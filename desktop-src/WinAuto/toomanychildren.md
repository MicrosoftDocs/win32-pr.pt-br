---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159887"
---
# <a name="toomanychildren"></a>TooManyChildren

## <a name="text"></a>Texto

Parou de procurar irmãos adicionais depois de encontrar {0} irmãos. Possível árvore incorreta

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

A árvore de elementos pode ser cíclica e a profundidade da árvore é infinita.

Esse problema pode causar problemas de navegação para ferramentas automatizadas porque elas irão inserir o que parece ser uma referência circular ou um loop infinito.

## <a name="possible-causes"></a>Possíveis causas

-   O design de aplicativo ou de controle pode ser muito complexo. Esse aviso pode ser relatado para controles de exibição de lista que têm um grande número de itens. Nesses casos, normalmente você pode ignorar esse aviso.
-   Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




