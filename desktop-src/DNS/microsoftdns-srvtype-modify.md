---
title: Método Modify da classe MicrosoftDNS_SRVType
description: O método Modify atualiza um registro de recurso de serviço (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_SRVType classe
- MicrosoftDNS_SRVType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009699"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Método Modify da classe MicrosoftDNS \_ SRVType

O método **Modify** atualiza um registro de recurso de serviço (SRV).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Prioridade* \[ do em, opcional\]
</dt> <dd>

Prioridade do host de destino especificado no nome do proprietário. Números inferiores implicam prioridades mais altas.

</dd> <dt>

*Peso* \[ em, opcional\]
</dt> <dd>

Peso do host de destino. Isso é útil ao selecionar entre os hosts que têm a mesma prioridade. As chances de usar esse host devem ser proporcionais ao seu peso.

</dd> <dt>

*Porta* \[ do em, opcional\]
</dt> <dd>

Porta usada no host de destino de um serviço de protocolo.

</dd> <dt>

*SRVDomainName* \[ em, opcional\]
</dt> <dd>

FQDN do host de destino. Um destino de \\ . \\ significa que o serviço está decididamente não disponível neste domínio.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referência ao novo objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Qualquer parâmetro não especificado permanece inalterado no registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe SRVType MicrosoftDNS**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





