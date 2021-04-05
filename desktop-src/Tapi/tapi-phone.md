---
description: A classe de dispositivo TAPI/telefone consiste em todos os dispositivos de telefone. Você acessa esses dispositivos usando as funções de telefone TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922211"
---
# <a name="tapiphone"></a>TAPI/telefone

A classe de dispositivo TAPI/telefone consiste em todos os dispositivos de telefone. Você acessa esses dispositivos usando as funções de telefone TAPI.

A função [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **DWSTRINGFORMAT** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

O membro **dwDeviceId** é o identificador do dispositivo de telefone associado ao identificador de telefone fornecido pelo [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

A função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) também preenche uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo **dwStringFormat** como StringFormat \_ Binary e acrescentando esse membro adicional:

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

O membro **adwDeviceIds** é uma matriz que contém os identificadores de dispositivo de todos os dispositivos de telefone associados ao dispositivo de linha especificado. Se não houver nenhum dispositivo de telefone associado, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) retornará o \_ valor de INVALDEVICECLASS LINEERR.

 

 



