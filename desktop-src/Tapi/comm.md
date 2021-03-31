---
description: A classe de dispositivo de comunicação consiste em portas de comunicação. Você acessa esses dispositivos usando as funções de arquivo e comunicação.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: Comentários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647524"
---
# <a name="comm"></a>Comentários

A classe de dispositivo de comunicação consiste em portas de comunicação. Você acessa esses dispositivos usando as funções de [arquivo](/windows/desktop/FileIO/file-management-functions) e [comunicação](/windows/desktop/DevIO/communications-functions).

A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor ASCII StringFormat e acrescentando uma cadeia de caracteres terminada em nulo que especifica o nome do dispositivo de comunicação (como o nome do modem).

 

 
