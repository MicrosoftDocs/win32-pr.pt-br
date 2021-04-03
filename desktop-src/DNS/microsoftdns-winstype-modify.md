---
title: Método Modify da classe MicrosoftDNS_WINSType
description: O método Modify atualiza um registro de recurso WINS (serviço de cadastramento na Internet do Windows).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_WINSType classe
- MicrosoftDNS_WINSType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824555"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Método Modify da \_ classe winstype MicrosoftDNS

O método **Modify** atualiza um registro de recurso WINS (serviço de cadastramento na Internet do Windows).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*MappingFlag* \[ em, opcional\]
</dt> <dd>

Sinalizador de mapeamento WINS que especifica se o registro deve ser incluído na replicação de zona. Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente. Os valores a seguir são válidos.



| Valor                                                                                                                                               | Significado                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Sinalizador de replicação<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Sinalizador sem replicação (registro local)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que um servidor DNS tenta resolução usando a pesquisa WINS.

</dd> <dt>

*CacheTimeout* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que um servidor DNS que usa a pesquisa WINS pode armazenar em cache a resposta do servidor WINS.

</dd> <dt>

*WinsServers* \[ em, opcional\]
</dt> <dd>

Lista de endereços IP separados por vírgulas de servidores WINS usados na pesquisa WINS.

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

[**MicrosoftDNS \_ winstype**](microsoftdns-winstype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe winstype MicrosoftDNS**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





