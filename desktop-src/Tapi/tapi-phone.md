---
description: A classe de dispositivo tapi/phone consiste em todos os dispositivos de telefone. Você acessa esses dispositivos usando as funções de telefone TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002714"
---
# <a name="tapiphone"></a>tapi/phone

A classe de dispositivo tapi/phone consiste em todos os dispositivos de telefone. Você acessa esses dispositivos usando as funções de telefone TAPI.

A [**função phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenche uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo o membro **dwStringFormat** como o valor BINARY STRINGFORMAT e adicionando \_ este membro adicional:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

O **membro dwDeviceId** é o identificador do dispositivo de telefone associado ao identificador de telefone dado por [**phoneGetID.**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)

A [**função lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) também preenche uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo **dwStringFormat** como STRINGFORMAT BINARY e adicionando \_ este membro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

O **membro adwDeviceIds** é uma matriz que contém os identificadores de dispositivo de todos os dispositivos de telefone associados ao dispositivo de linha determinado. Se não houver dispositivos de telefone associados, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) retornará o valor LINEERR \_ INVALDEVICECLASS.

 

 



