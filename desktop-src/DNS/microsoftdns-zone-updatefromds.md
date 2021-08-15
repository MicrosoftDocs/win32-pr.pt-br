---
title: Método UpdateFromDS da MicrosoftDNS_Zone classe
description: O método UpdateFromDS força uma atualização da zona do DS (Serviço de Diretório).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Método DNS UpdateFromDS
- Classe DNS do método UpdateFromDS, MicrosoftDNS_Zone dados
- MicrosoftDNS_Zone classe DNS , método UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca537c6440ae14d0e15dea28f62bdb919f3ed7e3348f3a64a2339e0668b5c8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957185"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Método UpdateFromDS da classe Zona \_ MicrosoftDNS

O **método UpdateFromDS** força uma atualização da zona do DS (Serviço de Diretório).

## <a name="syntax"></a>Sintaxe


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para executar esse método com êxito, ZoneType deve ser zero e a zona deve ser armazenada no DS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Zona \_ MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Método AgeAllRecords da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Método ChangeZoneType da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Método CreateZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Método ForceRefresh da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Método GetDistinguishedName da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Método PauseZone da classe zone \_ MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Método ReloadZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Método ResetSecondaries da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Método ResumeZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Método WriteBackZone da classe de zona \_ MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





