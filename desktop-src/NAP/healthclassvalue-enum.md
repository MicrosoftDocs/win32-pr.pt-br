---
title: Enumeração HealthClassValue (NapProtocol. h)
description: Indica o valor do TLV da classe de integridade.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue de enumeração de NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454597"
---
# <a name="healthclassvalue-enumeration"></a>Enumeração HealthClassValue

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O tipo de enumeração **HealthClassValue** indica o valor do TLV da classe de integridade.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**
</dt> <dd>

O TLV de classe de integridade é o firewall.

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**
</dt> <dd>

O TLV da classe de integridade é o nível de patch.

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**
</dt> <dd>

O TLV da classe de integridade é o antivírus.

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**
</dt> <dd>

O TLV da classe de integridade é atualização crítica.

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**
</dt> <dd>

Reservado somente para uso do sistema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |



 

 





