---
title: Serialização do conjunto de propriedades
description: Há duas versões do formato de serialização do conjunto de propriedades.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d8dfc1c51a6d33d6eb6f9c22b513a9a5397c87
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436281"
---
# <a name="property-set-serialization"></a>Serialização do conjunto de propriedades

Há duas versões do formato de serialização do conjunto de propriedades. A especificação original descreve a versão 0 do formato. Consulte [Versão de formato](format-version.md) para obter mais informações. A versão 1 estende a versão original. Todos os conjuntos de propriedades da versão 0 são válidos como conjuntos de propriedades da versão 1. O **campo Formatar** Versão no header de um conjunto de propriedades serializado indica a versão.

Os itens a seguir identificam as diferenças entre os formatos de serialização do conjunto de propriedades das versões 0 e 1.

-   Suporte para novos **valores VARTYPE.** Para obter mais informações sobre **valores VARTYPE** e como usá-los, consulte o tópico Tipos e estruturas de dados [IDispatch]( /previous-versions/ms221600(v=vs.100)) e a [**estrutura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

    Os seguintes **valores VARTYPE** não têm suporte em conjuntos de propriedades da versão 0, mas têm suporte na versão 1:

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    Além disso, SafeArrays pode ser serializado em um conjunto de propriedades. A presença de um SafeArray é indicada pelo bit VT_ARRAY combinado, usando uma operação **OR,** com os elementos de matriz no **membro vt** da [**estrutura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Por exemplo, um SafeArray de inteiros com sinal de 4 byte tem um tipo de VT_ARRAY \| VT_I4.

    Os seguintes tipos de elemento são válidos para um SafeArray em um conjunto de propriedades serializado:

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Quando o VT_VARIANT de dados é especificado, ele indica que o SafeArray em si contém estruturas [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Os tipos para esses elementos devem ser da lista anterior, exceto que não podem conter tipos VT_VARIANT aninhados.
    
    Observe que as implementações [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) devem ser capazes de se recuperar normalmente retornando um erro quando um novo tipo é encontrado; por exemplo, tipos VARENUM.

-   Nomes de propriedade sensíveis a minúsculas. Os nomes de propriedade, por exemplo, especificados no método [**IPropertyStorage::WritePropertyNames,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) não diferenciam minúsculas em conjuntos de propriedades da versão 0. Em conjuntos de propriedades da versão 1, os nomes de propriedade podem diferenciação de minúsculas, dependendo do valor da nova propriedade Comportamento.

    A propriedade Behavior é [ID da 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) com um tipo de VT_UI4. Se o bit mais baixo desse valor for definido, os nomes do conjunto de propriedades serão sensíveis a minúsculas. Defina PROPSETFLAG_CASE_SENSITIVE sinalizador de PROPSETFLAG_CASE_SENSITIVE no parâmetro *grfFlags* do método [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) para especificar um conjunto de propriedades sensíveis a minúsculas.

-   Nomes de propriedade longos. Os nomes de propriedade para conjuntos de propriedades da versão 0 devem ser menores ou iguais a 256 caracteres, incluindo o terminador de cadeia de caracteres, para conjuntos de propriedades na página de código Unicode. Se não estiver na página de código Unicode, eles deverão ter menos de 256 bytes. Os conjuntos de propriedades da versão 1, por outro lado, podem ter nomes de propriedade de comprimento ilimitado, embora ainda sejam limitados pelo limite geral de tamanho do conjunto de propriedades de 256 quilobytes (KB).

É recomendável que as implementações [**de IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) criem e mantenham conjuntos de propriedades da versão 0 por padrão. Se um chamador solicitar subsequentemente um recurso específico para o formato da versão 1, somente a versão do conjunto de propriedades deverá ser atualizada. Por exemplo, se uma propriedade do tipo VT_ARRAY for escrita ou se um nome de propriedade longo for gravado, a implementação deverá atualizar o formato do conjunto de propriedades para a versão 1. Uma exceção a essa diretriz ocorrerá se PROPSETFLAG_CASE_SENSITIVE valor de enumeração de PROPSETFLAG_CASE_SENSITIVE for especificado na chamada para [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Nesse caso, o conjunto de propriedades deve ser criado como um conjunto de propriedades da versão 1.

 

 