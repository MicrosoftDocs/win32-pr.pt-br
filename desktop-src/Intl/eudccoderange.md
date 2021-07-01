---
description: A chave do Registro EUDCCodeRange define intervalos de código euDC (caractere definido pelo usuário final) para várias páginas de código (conjuntos de caracteres).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120671"
---
# <a name="eudccoderange"></a>EUDCCodeRange

A chave do Registro EUDCCodeRange define intervalos de código [euDC (caractere](end-user-defined-characters.md) definido pelo usuário final) para várias páginas de código (conjuntos de caracteres). Ele é usado apenas por ferramentas que criam EUDCs e não é de interesse direto para usuários do EUDC. Essa chave do Registro tem o seguinte local do Registro:

HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange

O formato é:

EUDCCodeRange CodePage=FromTo \[ , FromTo\]

em que:



| Valor         | Descrição                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CodePage | Uma das cadeias de caracteres "932" (japonês), "936" (chinês simplificado), "949" (coreano), "950" (chinês tradicional) ou "Unicode" (Unicode). Não há suporte para outros valores.                                     |
| FromTo   | Valor da cadeia de caracteres que consiste em um par de valores hexadecimais de 4 dígitos separados por um hífen (-). Até quatro valores FromTo podem ser especificados, mas cada um deve ser separado do valor anterior por uma vírgula (,). |



 

A seguir estão os valores corretos para a entrada do Registro.


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entradas do Registro EUDC](eudc-registry-entries.md)
</dt> <dt>

[Eudc](eudc.md)
</dt> </dl>

 

 



