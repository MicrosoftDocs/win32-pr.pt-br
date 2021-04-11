---
title: Método createzone da classe MicrosoftDNS_Zone
description: O método createzone cria uma zona DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Método createzone DNS
- Método createzone DNS, classe MicrosoftDNS_Zone
- Classe de MicrosoftDNS_Zone de DNS, método createzone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009544"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Método createzone da classe de \_ zona MicrosoftDNS

O método **createzone** cria uma zona DNS.

## <a name="syntax"></a>Sintaxe


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome_da_Zona* \[ no\]
</dt> <dd>

Cadeia de caracteres que representa o nome da zona.

</dd> <dt>

*Zonatype* \[ no\]
</dt> <dd>

Tipo de zona. Os valores válidos são os seguintes:



| Valor                                                                        | Significado                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Integrado ao AD.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Zona secundária.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Zona de stub.<br/> **Windows Server 2003:** Esse tipo de zona é introduzido no Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Encaminhador de zona.<br/> **Windows Server 2003:** Esse tipo de zona é introduzido no Windows Server 2003.<br/> |



 

</dd> <dt>

*DsIntegrated* \[ no\]
</dt> <dd>

Indica se os dados de zona são armazenados no Active Directory ou em arquivos. Se for TRUE, os dados serão armazenados no Active Directory; Se for FALSE, os dados serão armazenados em arquivos.

</dd> <dt>

*DataFileName* \[ em, opcional\]
</dt> <dd>

Nome do arquivo de dados associado à zona.

</dd> <dt>

*IPADDR* \[ em, opcional\]
</dt> <dd>

Endereço IP do servidor DNS mestre para a zona.

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

[**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
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

 

 





