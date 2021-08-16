---
description: Todos os exemplos na documentação do SDK de criptografia são considerados como tendo as seguintes opções de \# inclusão e \# definição de diretivas do compilador.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#inclui e #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774271"
---
# <a name="includes-and-defines"></a>\#inclui e \# define

Todos os exemplos na documentação do SDK de criptografia são considerados como tendo as seguintes opções de **\# inclusão** e **\# definição** de diretivas do compilador.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Além disso, a constante do **\_ Win32 \_ WinNT** deve ser definida adequadamente. para obter mais informações sobre o **\_ WIN32 \_ WINNT**, consulte [usando os cabeçalhos de Windows](../winprog/using-the-windows-headers.md).

 

 
