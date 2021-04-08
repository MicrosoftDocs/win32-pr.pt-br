---
title: Atributo v1_enum
description: O atributo \ v1 \_ enum \ é direcionado que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum do atributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823279"
---
# <a name="v1_enum-attribute"></a>\_atributo de enumeração v1

O atributo de **\[ \_ enumeração \] v1** direciona que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a>Parâmetros

Este atributo não tem parâmetros.

## <a name="remarks"></a>Comentários

Usar o atributo de **\[ \_ enumeração \] v1** para transmitir um tipo enumerado como uma entidade de 32 bits aumenta a eficiência do marshaling e o desempacotamento de dados quando tal enumeração é inserida em estruturas ou uniões.

Para melhorar o desempenho, é recomendável aplicar o atributo de **\[ \_ enumeração \] v1** a enumeradores em aplicativos de 32 bits. No entanto, tenha em mente que, em plataformas de 16 bits, o compilador C trata um tipo enumerado como um [**int**](int.md)de 16 bits. Portanto, os aplicativos cliente de 16 bits precisam converter os tipos de [**Enumeração**](enum.md) [**para a transmissão**](long.md) remota a fim de evitar a substituição de dados ou o envio de valores incorretos.

## <a name="examples"></a>Exemplos

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**enumera**](enum.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Longas**](long.md)
</dt> </dl>

 

 




