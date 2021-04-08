---
description: A API do Gerenciador de identidades do par permite que você crie, enumere e manipule identidades pares em um aplicativo par.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Sobre o Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828417"
---
# <a name="about-identity-manager"></a>Sobre o Identity Manager

A API do Gerenciador de identidades do par permite que você crie, enumere e manipule identidades pares em um aplicativo par. Você pode usar as identidades de par criadas usando essa API como entrada para as APIs do provedor de namespace par e PNRP (Peer Name Resolution Protocol).

## <a name="peer-identity-manager-best-practices"></a>Práticas recomendadas do Gerenciador de identidade do par

Cada usuário deve ter algumas identidades pares que podem usar para as atividades do par. Por exemplo, um usuário pode ter duas identidades pares para trabalho e lazer.

Um aplicativo de par bem projetado permite que um usuário selecione uma identidade de par a ser usada. Um usuário poderá criar uma nova identidade de par se nenhuma identidade de par existente for apropriada para uso com um aplicativo.

Um aplicativo par bem projetado também controla o número de identidades que ele cria. Se um aplicativo criar uma identidade de par temporária, o aplicativo deverá excluir a identidade do par quando a identidade não for necessária. Se um aplicativo não executar essa manutenção, o Gerenciador de identidade do par poderá não ser capaz de criar identidades pares até que algumas identidades de mesmo nível sejam removidas.

 

 



