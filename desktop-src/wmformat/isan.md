---
title: ISAN
description: O atributo ISAN contém o número de audiovisual internacional padrão (ISAN) que identifica o conteúdo.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de mídia do Windows do ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365661"
---
# <a name="isan"></a>ISAN

O atributo **Isan** contém o número de audiovisual internacional padrão (Isan) que identifica o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszISAN

## <a name="data-type"></a>Tipo de Dados

**Cadeia de caracteres do \_ tipo WMT \_**

## <a name="remarks"></a>Comentários

O ISAN é um padrão internacional para identificar o audiovisual Works. Para obter informações sobre o ISAN, visite o [site da Web](https://www.isan.org/)do padrão.

O objeto editor de metadados verifica a cadeia de caracteres de ISAN quando você define esse atributo. A formatação de cadeia de caracteres aceitável, conforme descrito na seção 4,1 da especificação de ISAN, consiste em 16 dígitos hexadecimais, opcionalmente separados por espaços em branco ou hifens em segmentos de 4 dígitos. O número formatado deve ser seguido, opcionalmente separado por um espaço ou hífen, por um caractere de verificação válido. O caractere de verificação pode ser um dígito decimal ou uma letra maiúscula. Consulte anexo a do guia do usuário do ISAN para obter informações sobre como derivar o número do cheque.

A cadeia de caracteres de ISAN padrão pode ser seguida pelas informações de versão. Se houver, as informações de versão consistem em oito dígitos hexadecimais seguidos de um número de cheque. A formatação desses caracteres segue as mesmas regras que a cadeia de caracteres básica.

## <a name="examples"></a>Exemplos

A seguir estão três cadeias de caracteres formatadas de forma aceita para um exemplo de ISAN.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



A cadeia de caracteres a seguir mostra o formato de um ISAN com informações de versão.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




