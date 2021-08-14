---
title: Florestas
description: Uma floresta é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- florestas do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ccccbce1c660c3f1e185e75971aa71d613c2db012ce42979cfaee7cd9c2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189196"
---
# <a name="forests"></a>Florestas

Uma [*floresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo. Todas as árvores em uma floresta compartilham um esquema, configuração e catálogo global comuns. Todas as árvores em uma determinada relação de confiança de troca de floresta de acordo com relações de confiança kerberos hierárquicas transitivas. Ao contrário das árvores, uma floresta não requer um nome distinto. Existe uma floresta como um conjunto de objetos de referência cruzada e relações de confiança Kerberos reconhecidas pelas árvores de membro. Árvores em uma floresta formam uma hierarquia para fins de confiança Kerberos; o nome da árvore na raiz da árvore de confiança refere-se a uma determinada floresta.

A figura a seguir mostra uma floresta de namespaces não contíguos.

![floresta de namespaces não contíguos](images/forests.png)

 

 