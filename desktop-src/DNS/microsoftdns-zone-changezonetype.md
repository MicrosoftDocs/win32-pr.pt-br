---
title: Método ChangeZoneType da classe MicrosoftDNS_Zone
description: O método ChangeZoneType altera o tipo de uma zona.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- DNS do método ChangeZoneType
- Método ChangeZoneType DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009246"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Método ChangeZoneType da classe de \_ zona MicrosoftDNS

O método **ChangeZoneType** altera o tipo de uma zona.

## <a name="syntax"></a>Sintaxe


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Zonatype* \[ no\]
</dt> <dd>

Tipo de zona. Os valores válidos são os seguintes:



| Valor                                                                        | Significado                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Zona primária.<br/>   |
| <dl> <dt>1</dt> </dl> | Zona secundária.<br/> |
| <dl> <dt>2</dt> </dl> | Zona de stub.<br/>      |
| <dl> <dt>3</dt> </dl> | Encaminhador de zona.<br/> |



 

</dd> <dt>

*DataFileName* \[ em, opcional\]
</dt> <dd>

Nome do arquivo de dados associado à zona.

</dd> <dt>

*IPADDR* \[ em, opcional\]
</dt> <dd>

Endereço IP do servidor DNS do mate para a zona.

</dd> <dt>

*AdminEmailName* \[ em, opcional\]
</dt> <dd>

Endereço de email do administrador responsável pela zona.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR do tipo **MicrosoftDns \_ Zone**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

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

[**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
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

 

 





