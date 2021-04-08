---
title: Gerenciando Propriedades
description: Cada propriedade consiste em um identificador de propriedade (exclusivo dentro de seu conjunto de propriedades), uma marca de tipo Variant (VT ou VarType) que representa o tipo de um valor e o próprio valor.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- Armazenamento estruturado Strctd STG, usando, gerenciando Propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10dd78a1f8a8484090728dba6fe149840e940461
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823831"
---
# <a name="managing-properties"></a>Gerenciando Propriedades

Cada propriedade consiste em um *identificador de propriedade* (exclusivo dentro de seu conjunto de propriedades), uma *marca de tipo Variant (VT ou VARTYPE)* que representa o tipo de um valor e o próprio *valor* . A marca tipo Variant descreve a representação dos dados no valor. Além disso, uma propriedade também pode ser atribuída a um *nome de cadeia de caracteres* que pode ser usado para identificar a propriedade, em vez de usar o identificador de propriedade numérica (ID) necessário. Para criar e gerenciar Propriedades, COM define a interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .

A interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) inclui métodos para ler e gravar matrizes de propriedades ou nomes de propriedade. A interface inclui os métodos [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) e [**REVERT**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) que são semelhantes aos métodos [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de mesmo nome. Há métodos de utilitário que permitem definir o identificador de classe (CLSID) do conjunto de propriedades, definir os horários associados ao conjunto e obter estatísticas sobre o conjunto de propriedades. Por fim, o método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) cria um enumerador e retorna um ponteiro para sua interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) . Você pode chamar os métodos dessa interface para enumerar estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) em seu objeto, o que fornecerá informações sobre todas as propriedades no conjunto de propriedades atual.

Veja a seguir um exemplo de como as propriedades são representadas. Se uma propriedade específica em um conjunto de propriedades mantiver o nome científico de um animal, esse nome poderá ser armazenado como uma cadeia de caracteres terminada em zero. Armazenado junto com o nome seria um indicador de tipo para indicar que o valor é uma cadeia de caracteres terminada em zero. Essas propriedades podem ter as seguintes características:



| ID da propriedade | Identificador de cadeia de caracteres | Indicador de tipo | Valor representado              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | DTI \_ animalName   | LPWStr do VT \_     | Cadeia de caracteres Unicode terminada em zero |
| 03          | DTI \_ LEGCOUNT     | \_I2 VT         | WORD                           |



 

Qualquer aplicativo que reconheça o formato do conjunto de propriedades — identificá-lo por meio de seu identificador de formato (FMTID) — pode examinar a propriedade com um identificador de PID \_ animalName, determinar que ele é uma cadeia de caracteres terminada com zero e ler e gravar o valor. Embora o aplicativo possa chamar [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) para ler qualquer ou todas as propriedades definidas (tendo obtido primeiro um ponteiro), o aplicativo deve saber como interpretar o conjunto de propriedades.

Um valor de propriedade é passado por meio de interfaces de propriedade como uma instância do tipo [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).

É importante distinguir entre essas propriedades armazenadas (persistentes) e as propriedades de tempo de execução. Constantes de valor de tipo Variant têm nomes que começam com VT \_ . O conjunto de PROPVARIANTs válido, no entanto, não é totalmente equivalente ao conjunto de VARIAntes usado na automação e nos controles ActiveX.

A única diferença entre as duas estruturas é o conjunto permitido de marcas VT \_ (Variant Type/VARTYPE) em cada. Onde um determinado tipo de propriedade pode ser usado em uma variante e em um PROPVARIANT, a marca de tipo (o valor de VT \_ ) sempre tem um valor idêntico. Além disso, para um determinado \_ valor de VT, a representação na memória usada em variantes e PROPVARIANTs é idêntica. Juntos, essa abordagem permite que o sistema de tipos pegue marcas de tipo não permitido, enquanto, ao mesmo tempo, permite que um cliente experiente implemente uma conversão de ponteiro quando apropriado.

Para obter mais informações, consulte a seção a seguir [considerações de armazenamento de propriedade](property-storage-considerations.md).

 

 