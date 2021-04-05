---
title: Método Modify da classe MicrosoftDNS_WKSType
description: O método Modify atualiza um registro de recurso de serviços de Well-Known (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824552"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Método Modify da classe MicrosoftDNS \_ WKSType

O método **Modify** atualiza um registro de recurso de serviços de Well-Known (WKS).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*InternetAddress* \[ em, opcional\]
</dt> <dd>

Endereço IP da Internet para o proprietário do registro.

</dd> <dt>

*IPProtocol* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o protocolo IP para este registro. Os valores válidos são UDP ou TCP.

</dd> <dt>

*Serviços* \[ do em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (serviço bem conhecido).

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe WKSType MicrosoftDNS**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





