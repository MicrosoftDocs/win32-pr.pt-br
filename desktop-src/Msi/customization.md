---
description: Como o instalador Windows mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ece84afd2b9ca5ce547d9ea96aed23786f78c89f01f5b5b5eaa78e2791e86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947850"
---
# <a name="customization"></a>Personalização

Como o instalador Windows mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote. As transformação podem ser usadas para encapsular as várias personalizações de um pacote base exigido por diferentes grupos de trabalho. Para obter mais informações, consulte [Merges and Transforms](merges-and-transforms.md).

Várias transformares de um pacote base podem ser aplicadas em tempo real durante a instalação. Isso fornece um mecanismo para atribuir com eficiência instalações personalizadas a diferentes grupos de usuários. Por exemplo, isso seria útil em organizações em que os departamentos de suporte financeiro e de equipe exigem instalações diferentes de um produto específico. O produto pode ser disponibilizado para todos [](administrative-installation.md) na organização por meio de uma instalação administrativa do pacote base em um único ponto de instalação administrativa. Cada grupo de trabalho pode receber automaticamente sua personalização apropriada por meio de uma transformação em tempo real ao instalar o produto.

 

 



