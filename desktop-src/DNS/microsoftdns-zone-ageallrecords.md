---
title: Método AgeAllRecords da classe MicrosoftDNS_Zone
description: O método AgeAllRecords habilita a duração de alguns ou todos os registros não NS e não SOA em uma zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS do método AgeAllRecords
- Método AgeAllRecords DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455733"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>Método AgeAllRecords da classe de \_ zona MicrosoftDNS

O método **AgeAllRecords** habilita a duração de alguns ou todos os registros não ns e não soa em uma zona.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NodeName* \[ em, opcional\]
</dt> <dd>

Nome do nó para idade.

</dd> <dt>

*ApplyToSubtree* \[ em, opcional\]
</dt> <dd>

Especifica se o envelhecimento deve ser aplicado a todos os registros na subárvore. Defina como TRUE para aplicar a duração a todos os registros na subárvore, começando com NodeName.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

\_O êxito do erro indica que a expiração foi concluída com êxito. Qualquer outro valor é um código de erro.

## <a name="remarks"></a>Comentários

Se *NodeName* não for especificado, todos os registros estarão sujeitos à expiração e à eliminação.

Se *NodeName* for especificado e *ApplyToSubtree* não for especificado ou definido como zero, os registros no nó especificado estarão sujeitos à expiração e à eliminação.

Se *NodeName* for especificado e *ApplyToSubtree* for definido como 1, todos os registros da subárvore começando em *NodeName* estarão sujeitos à expiração e à eliminação. O carimbo de data/hora é definido como a hora atual para todos os RRs não NS e não SOA com os nomes de proprietário identificados pelos parâmetros de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Zona MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método createzone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Método WriteBackZone da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





