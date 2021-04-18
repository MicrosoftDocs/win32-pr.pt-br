---
title: CCLSOBJ. CPP
description: No componente de provedor de exemplo, as funções para o objeto de classe de esquema estão contidas em cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771762"
---
# <a name="cclsobjcpp"></a>CCLSOBJ. CPP

No componente de provedor de exemplo, as funções para o objeto de classe de esquema estão contidas em cclsobj. cpp.

A classe **CSampleDSClass** está definida neste arquivo. **CSampleDSClass** é definido com métodos e propriedades listados na tabela a seguir.



| Método                      | Descrição                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSClass**          | Construtor padrão.                                                                                                                                                                                      |
| **~ CSampleDSClass**         | Destruidor padrão.                                                                                                                                                                                       |
| **Createclass**             | Crie um objeto de classe de esquema ADs. Definições de atributo de pesquisa chamando **SampleDSGetClassDefinition**.                                                                                                 |
| **Createclass**             | Crie um objeto de classe de esquema, dadas as definições de atributo, definindo atributos conhecidos, como aqueles listados em [**IADsClass:: mandatoryattributes**](iadsclass-property-methods.md).                     |
| **AllocateClassObject**     | Crie um objeto de classe de esquema e carregue seus dados de tipo.                                                                                                                                                       |
| **QueryInterface**          | Retorne o ponteiro de interface solicitado, se disponível.                                                                                                                                                      |
| Métodos IADs padrão.      | Métodos de interface padrão [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) incluídos neste arquivo.                                                                                                                                     |
| Métodos IADsClass padrão. | Métodos de interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) padrão incluídos neste arquivo.                                                                                                                           |
| **Createpropertylist**      | Crie uma lista de propriedades associadas a essa classe de esquema chamando **CreatePropertyEntry**.                                                                                                          |
| **CreatePropertyEntry**     | Crie um objeto de propriedade nesta classe de esquema.                                                                                                                                                           |
| **FreePropertyEntry**       | Libere a entrada feita em **CreatePropertyEntry**.                                                                                                                                                            |
| **MakeVariantFromPropList** | Crie uma matriz de VARIAntes na lista de propriedades criada por **Createpropertylist**. Pode ser usado na implementação de [**IADsClass:: mandatoryattributes**](iadsclass-property-methods.md) e assim por diante. |



 

 

 




