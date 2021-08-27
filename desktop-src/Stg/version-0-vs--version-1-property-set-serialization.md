---
title: Serialização do conjunto de propriedades
description: Há duas versões do formato de serialização do conjunto de propriedades.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f340b31252bfc3d99f72746e8ae791f313498c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989149"
---
# <a name="property-set-serialization"></a>Serialização do conjunto de propriedades

Há duas versões do formato de serialização do conjunto de propriedades. A especificação original descreve a versão 0 do formato. Consulte [Formatar versão](format-version.md) para obter mais informações. A versão 1 estende a versão original. Todos os conjuntos de propriedades da versão 0 são válidos como conjuntos de propriedades da versão 1. O campo **versão de formato** no cabeçalho de um conjunto de propriedades serializadas indica a versão.

Os itens a seguir identificam as diferenças entre a versão 0 e os formatos de serialização do conjunto de propriedades da versão 1.

-   Suporte para novos valores **VarType** . Para obter mais informações sobre valores **VarType** e como usá-los, consulte o tópico [tipos de dados e estruturas do IDispatch]( /previous-versions/ms221600(v=vs.100)) e a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

    Os seguintes valores **VarType** não têm suporte nos conjuntos de propriedades da versão 0, mas têm suporte na versão 1:

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    Além disso, SafeArrays podem ser serializados em um conjunto de propriedades. A presença de um SafeArray é indicada pelo bit de VT_ARRAY combinado, usando uma operação **ou** , com os elementos da matriz no membro **VT** da estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Por exemplo, um SafeArray de inteiros com sinal de 4 bytes tem um tipo de VT_ARRAY \| VT_I4.

    Os seguintes tipos de elemento são válidos para um SafeArray em um conjunto de propriedades serializadas:

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Quando o tipo de dados VT_VARIANT é especificado, ele indica que o SafeArray em si contém estruturas [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Os tipos desses elementos devem ser da lista anterior, exceto que não podem conter tipos de VT_VARIANT aninhados.
    
    Observe que as implementações de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) devem ser capazes de recuperar normalmente retornando um erro quando um novo tipo é encontrado; por exemplo, VARENUM Types.

-   Nomes de propriedade diferenciar maiúsculas e minúsculas. Os nomes de propriedade, por exemplo, aqueles especificados no método [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) , não diferenciam maiúsculas de minúsculas nos conjuntos de propriedades da versão 0. Nos conjuntos de propriedades da versão 1, os nomes de propriedade podem diferenciar maiúsculas de minúsculas, dependendo do valor da nova propriedade de comportamento.

    A propriedade Behavior é a [ID de propriedade 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) com um tipo de VT_UI4. Se o menor bit desse valor for definido, os nomes do conjunto de propriedades diferenciarão maiúsculas de minúsculas. Defina o sinalizador PROPSETFLAG_CASE_SENSITIVE no parâmetro *grfFlags* do método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para especificar um conjunto de propriedades que diferencia maiúsculas de minúsculas.

-   Nomes de propriedade longos. Os nomes de propriedade dos conjuntos de propriedades da versão 0 devem ser menores ou iguais a 256 caracteres, incluindo o terminador de cadeia de caracteres, para conjuntos de propriedades na página de código Unicode. Se não estiver na página de código Unicode, eles deverão ter menos de 256 bytes. Por outro lado, os conjuntos de propriedades da versão 1 podem ter nomes de propriedade de comprimento ilimitado, embora eles ainda sejam limitados pelo limite de tamanho do conjunto de propriedades geral de 256 kilobytes (KB).

É recomendável que as implementações de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) criem e mantenham os conjuntos de propriedades da versão 0 por padrão. Em seguida, se um chamador solicitar um recurso específico para o formato da versão 1, somente a versão do conjunto de propriedades deverá ser atualizada. Por exemplo, se uma propriedade do tipo VT_ARRAY for gravada ou se um nome de propriedade longo for gravado, a implementação deverá atualizar o formato do conjunto de propriedades para a versão 1. Uma exceção a essa diretriz ocorre se o valor de enumeração de PROPSETFLAG_CASE_SENSITIVE for especificado na chamada para [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Nesse caso, o conjunto de propriedades deve ser criado como um conjunto de propriedades da versão 1.

 

 
