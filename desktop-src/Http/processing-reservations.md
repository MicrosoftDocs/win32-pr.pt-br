---
title: Processing Reservations
description: As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no armazenamento de reservas persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393758"
---
# <a name="processing-reservations"></a>Processing Reservations

As reservas para partes do namespace da URL são feitas pelo administrador do sistema e colocadas no armazenamento de reservas persistente. A raiz do namespace de URL para HTTP pertence ao administrador do sistema. Para todos os valores de host e porta, as duas reservas a seguir são sempre assumidas na raiz do namespace **relativeUri.**



| Namespace reservado                 | Reservado para              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Administrador do LocalSystem |
| https:// <host> :<port>/ | Administrador do LocalSystem |



 

Essas reservas implícitas não podem ser removidas. No entanto, é possível delegar reservas raiz explícitas a outros usuários. Reservas como as seguintes criariam essas delegações:



| Namespace reservado        | Reservado para |
|---------------------------|--------------|
| `https://+:80/`           | UserA, UserC |
| `https://adatum.com:443/` | Userb        |



 

Se essas reservas delegadas são removidas pelo administrador do sistema, a propriedade do namespace reverte para a reserva implícita para os valores de host e porta correspondentes.

 

 




