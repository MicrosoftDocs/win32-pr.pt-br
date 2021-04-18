---
description: A chave do registro EUDCCodeRange define intervalos de código EUDC (caracteres definidos pelo usuário final) para várias páginas de código (conjuntos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760360"
---
# <a name="eudccoderange"></a>EUDCCodeRange

A chave do registro EUDCCodeRange define intervalos de código [EUDC (caracteres definidos pelo usuário final)](end-user-defined-characters.md) para várias páginas de código (conjuntos de caracteres). Ele é usado somente por ferramentas que criam EUDCs e não é de preocupação direta com os usuários do EUDC. Essa chave do registro tem o seguinte local de registro:

HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

O formato é:

EUDCCodeRange CodePage = FromTo \[ , deto\]

onde:



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Uma das cadeias de caracteres "932" (japonês), "936" (chinês simplificado), "949" (coreano), "950" (chinês tradicional) ou "Unicode" (Unicode). Não há suporte para nenhum outro valor.                                     |
| Deto   | Valor da cadeia de caracteres que consiste em um par de valores hexadecimais de 4 dígitos separados por um hífen (-). Até quatro valores deto podem ser especificados, mas cada um deve ser separado do valor anterior por uma vírgula (,). |



 

A seguir estão os valores corretos para a entrada do registro.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entradas do registro EUDC](eudc-registry-entries.md)
</dt> <dt>

[EUDC](eudc.md)
</dt> </dl>

 

 



