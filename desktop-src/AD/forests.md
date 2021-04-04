---
title: Florestas
description: Uma floresta é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Active Directory de florestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917128"
---
# <a name="forests"></a>Florestas

Uma [*floresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) é um conjunto de uma ou mais árvores de domínio que não formam um namespace contíguo. Todas as árvores em uma floresta compartilham um esquema, uma configuração e um catálogo global comuns. Todas as árvores em uma determinada floresta de confiança do Exchange de acordo com relações de confiança Kerberos hierárquicas transitivas. Ao contrário das árvores, uma floresta não requer um nome distinto. Existe uma floresta como um conjunto de objetos de referência cruzada e relações de confiança Kerberos reconhecidas pelas árvores de membros. As árvores em uma floresta formam uma hierarquia para fins de confiança Kerberos; o nome da árvore na raiz da árvore de confiança refere-se a uma determinada floresta.

A figura a seguir mostra uma floresta de namespaces não contíguos.

![floresta de namespaces não contíguos](images/forests.png)

 

 