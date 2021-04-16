---
title: Editar sessões
description: Quando um serviço de texto deve obter, modificar ou definir texto em um contexto, ele deve solicitar uma sessão de edição.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- TSF (estrutura de serviços de texto), editar sessão
- TSF (estrutura de serviços de texto), editar sessão
- serviços de texto, sessão de edição
- sessão de edição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498798"
---
# <a name="edit-sessions"></a>Editar sessões

Quando um serviço de texto deve obter, modificar ou definir texto em um contexto, ele deve solicitar uma *sessão de edição*. Quando uma sessão de edição é solicitada, o Gerenciador de TSF negocia com o proprietário do contexto de destino para um bloqueio de documento do tipo solicitado. Quando o bloqueio de documento é concedido, o Gerenciador de TSF permite que o serviço de texto Leia e/ou grave texto de ou para o contexto.

 

 




