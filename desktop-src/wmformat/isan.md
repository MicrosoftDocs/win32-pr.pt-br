---
title: Isan
description: O atributo ISAN contém o ISAN (International Standard Audiovisual Number) que identifica o conteúdo.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de mídia do Windows ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2af088938219ed48f2b281c627c0b64cc8e13fdea630b54a51a6f23db1b448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808816"
---
# <a name="isan"></a>Isan

O **atributo ISAN** contém o ISAN (International Standard Audiovisual Number) que identifica o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszISAN

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O ISAN é um padrão internacional para identificar trabalhos audiovisuais. Para obter informações sobre o ISAN, visite o [site do padrão.](https://www.isan.org/)

O objeto do editor de metadados verifica a cadeia de caracteres ISAN ao definir esse atributo. A formatação de cadeia de caracteres aceitável, conforme descrito na seção 4.1 da especificação ISAN, consiste em 16 dígitos hexadecimais, opcionalmente separados por espaço em branco ou hifens em segmentos de 4 dígitos. O número formatado deve ser seguido, também opcionalmente separado por um espaço ou hífen, por um caractere de verificação válido. O caractere de verificação pode ser um dígito decimal ou uma letra maiúscula. Consulte o anexo A do guia do usuário isan para obter informações sobre como derivar o número de verificação.

A cadeia de caracteres ISAN padrão pode ser seguida por informações de versão. Se presente, as informações de versão consistem em oito dígitos hexadecimais seguidos por um número de verificação. A formatação desses caracteres segue as mesmas regras que a cadeia de caracteres básica.

## <a name="examples"></a>Exemplos

A seguir estão três cadeias de caracteres formatadas de forma aceitável para um ISAN de exemplo.


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

 

 




