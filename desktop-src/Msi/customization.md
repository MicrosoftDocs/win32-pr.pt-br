---
description: Como o Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756735"
---
# <a name="customization"></a>Personalização

Como o Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote. As transformações podem ser usadas para encapsular as várias personalizações de um pacote base exigido por diferentes grupos de dados. Para obter mais informações, consulte [mesclagens e transformações](merges-and-transforms.md).

Várias transformações de um pacote base podem ser aplicadas imediatamente durante a instalação. Isso fornece um mecanismo para atribuir com eficiência instalações personalizadas a diferentes grupos de usuários. Por exemplo, isso seria útil em organizações nas quais os departamentos de suporte da equipe e Finanças exigem diferentes instalações de um produto específico. O produto pode ser disponibilizado para todos na organização por uma [instalação administrativa](administrative-installation.md) do pacote base para um único ponto de instalação administrativa. Cada grupo de trabalho pode, então, receber automaticamente sua personalização apropriada por meio de uma transformação imediata ao instalar o produto.

 

 



