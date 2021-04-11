---
title: Método Modify da classe MicrosoftDNS_ATMAType
description: O método Modify atualiza um endereço ATM para um registro de recurso de nome (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_ATMAType classe
- MicrosoftDNS_ATMAType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009380"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Método Modify da classe MicrosoftDNS \_ ATMAType

O método **Modify** atualiza um endereço ATM para um registro de recurso de nome (ATMA).

## <a name="syntax"></a>Sintaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TTL* \[ em, opcional\]
</dt> <dd>

Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.

</dd> <dt>

*Formato* \[ em, opcional\]
</dt> <dd>

Formato de endereço ATM. Dois valores possíveis para o formato são: 0 indicando o formato de endereço do sistema final do ATM (AESA) e 1 indicando o formato E. 164.

</dd> <dt>

*ATMAddress* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres de comprimento variável de octetos que contém o endereço ATM do nó/proprietário ao qual esse RR pertence. Os primeiros quatro bytes da matriz são usados para armazenar o tamanho da cadeia de caracteres do octeto. O byte mais significativo é armazenado em byte 0.

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

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData da \_ classe ATMAType MicrosoftDNS**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





