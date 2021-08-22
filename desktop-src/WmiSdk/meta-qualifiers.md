---
description: Os metaqualificadores refinam a definição de metaconstruções no modelo CIM, esclarecendo o uso real de uma classe ou declaração de propriedade dentro da sintaxe do MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Metaqualificadores
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76609fecca3e3831372ea813e7210cd449c2e1e4fc527df605bc523efd4c1be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131168"
---
# <a name="meta-qualifiers"></a>Metaqualificadores

Os metaqualificadores refinam a definição de metaconstruções no modelo CIM, esclarecendo o uso real de uma classe ou declaração de propriedade dentro da sintaxe do MOF.

<dt>

<span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Associação**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe é uma classe de associação usada para descrever uma relação entre duas outras classes. A ausência desse qualificador indica que a classe não é uma classe de associação. Esse qualificador é mutuamente exclusivo com a **indicação**. Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).

</dd> <dt>

<span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indicações**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe de objeto define uma indicação. Esse qualificador é mutuamente exclusivo com **Associação**. O padrão é **false**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

 




