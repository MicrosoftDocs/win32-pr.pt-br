---
title: Processando reservas
description: As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no repositório de reserva persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104366887"
---
# <a name="processing-reservations"></a>Processando reservas

As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no repositório de reserva persistente. A raiz do namespace da URL para HTTP pertence ao administrador do sistema. Para todos os valores de porta e host, as duas reservas a seguir são sempre presumidas na raiz do namespace **relativeUri** .



| Namespace reservado                 | Reservado para              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Administrador LocalSystem |
| https:// <host> :<port>/ | Administrador LocalSystem |



 

Essas reservas implícitas não podem ser removidas. No entanto, é possível delegar reservas de raiz explícitas a outros usuários. As reservas, como a seguir, criaria tais delegações:



| Namespace reservado        | Reservado para |
|---------------------------|--------------|
| `https://+:80/`           | UserA, UserC |
| `https://adatum.com:443/` | UserB        |



 

Se essas reservas delegadas forem removidas pelo administrador do sistema, a propriedade do namespace será revertida para a Reserva implícita para os valores de host e porta correspondentes.

 

 




