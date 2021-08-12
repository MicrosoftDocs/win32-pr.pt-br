---
description: A lista a seguir lista os valores possíveis do campo Sinalizadores em uma ACE (Entrada de Controle de Acesso) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes de sinalizador ACE do namespace (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 7b4051a6c17e9861d656207335b2543cf7d886e74569c269df2a4f680f47fbe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555176"
---
# <a name="namespace-ace-flag-constants"></a>Constantes de sinalizador ACE do namespace

A lista a seguir lista os valores possíveis do campo **Sinalizadores** em uma ACE (Entrada de Controle de Acesso) WMI.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Objetos filho não contêiner herdam a ACE como uma ACE efetiva.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



A ACE tem um efeito sobre namespaces filho, bem como o namespace atual.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**SEM \_ PROPAGAR \_ HERDAR \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



A ACE aplica-se somente ao namespace atual e aos filhos imediatos.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT \_ ONLY \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



A ACE aplica-se somente a namespaces filho.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**\_ACE HERDADO**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Isso não é definido pelos clientes, mas é relatado aos clientes quando a origem de uma ACE é um namespace pai.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança WMI](wmi-security-constants.md)
</dt> <dt>

[Definindo Descritores de Segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




