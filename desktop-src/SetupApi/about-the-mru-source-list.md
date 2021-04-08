---
description: A lista de origem usada mais recentemente (MRU) permanece residente no sistema de usuários.
ms.assetid: 010f8f88-999e-4dde-bffb-ac1a07256d55
title: Sobre a lista de origem do MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062624057e7dd1a083ebf0eb152200fd3a7241b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920842"
---
# <a name="about-the-mru-source-list"></a>Sobre a lista de origem do MRU

A lista de origem usada mais recentemente (MRU) permanece residente no sistema do usuário. As funções de instalação manipulam internamente a criação de novas listas de origem e sua localização na máquina do usuário. As funções de instalação usam essa lista para armazenar informações sobre caminhos de origem usados em instalações anteriores.

Você pode usar essas informações ao solicitar ao usuário um caminho de origem. Por exemplo, você pode criar uma lista suspensa das conexões de rede usadas como caminhos de origem em instalações anteriores.

Dependendo de suas permissões, você pode criar uma lista de usuários, uma que seja específica a um usuário específico, ou uma lista do sistema, uma que seja a mesma para todos os usuários. Além das listas de origem do sistema e do usuário, você pode criar uma lista de origem temporária que é descartada quando o aplicativo de instalação é encerrado.

 

 



