---
description: O campo comprimento em um TLV terceto identifica o número de bytes codificados no campo valor.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Comprimento codificado e bytes de valor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44ec9892e9407cbe587dbb60219b758ac95392e64dfabcf4866e02a1ad9343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904466"
---
# <a name="encoded-length-and-value-bytes"></a>Comprimento codificado e bytes de valor

O campo *comprimento* em um TLV terceto identifica o número de bytes codificados no campo *valor* . O campo *valor* contém o conteúdo que está sendo enviado entre computadores. Se o campo de *valor* contiver menos de 128 bytes, o campo *comprimento* exigirá apenas um byte. O bit 7 do campo de *comprimento* é zero (0) e os bits restantes identificam o número de bytes de conteúdo que está sendo enviado. Se o campo de *valor* contiver mais de 127 bytes, o bit 7 do campo de *comprimento* será um (1) e os bits restantes identificarão o número de bytes necessários para conter o comprimento. Os exemplos são mostrados na ilustração a seguir.

![byte de comprimento de TLV der](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de transferência de DER](about-der-transfer-syntax.md)
</dt> <dt>

[Bytes de marca codificados](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



