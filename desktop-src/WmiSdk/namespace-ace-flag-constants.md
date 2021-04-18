---
description: A lista a seguir lista os possíveis valores do campo Flags em uma ACE (entrada de controle de acesso) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes do sinalizador ACE do namespace (WinNT. h)
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
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750141"
---
# <a name="namespace-ace-flag-constants"></a>Constantes do sinalizador ACE do namespace

A lista a seguir lista os possíveis valores do campo **flags** em uma ACE (entrada de controle de acesso) WMI.

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**\_ACE de herança de objeto \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Os objetos filho sem contêiner herdam a ACE como uma ACE efetiva.


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**\_Ace herdar contêiner \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



A ACE tem um efeito nos namespaces filho, bem como no namespace atual.


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NENHUMA \_ ACE de \_ herança de propagação \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



A ACE aplica-se somente ao namespace atual e aos filhos imediatos.


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**HERDAr \_ somente \_ Ace**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



A ACE aplica-se somente a namespaces filho.


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**Ace HERDAdo \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Isso não é definido pelos clientes, mas é relatado para clientes quando a origem de uma ACE é um namespace pai.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




