---
description: Contém informações sobre uma assinatura digital.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Estrutura de SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169691"
---
# <a name="signer_signature_info-structure"></a>Estrutura de informações de \_ assinatura do assinante \_

A estrutura de **\_ \_ informações de assinatura do assinante** contém informações sobre uma assinatura digital.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**algidHash**
</dt> <dd>

O algoritmo de hash usado para a assinatura digital.

</dd> <dt>

**dwAttrChoice**
</dt> <dd>

Especifica se a assinatura tem atributos de [*Authenticode*](../secgloss/a-gly.md) . Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                      | Significado                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**Signatário \_ FATORES \_ attr**</dt> <dt>1</dt> </dl> | A assinatura tem atributos de [*Authenticode*](../secgloss/a-gly.md) .<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**Signatário \_ SEM \_ attr**</dt> <dt>0</dt> </dl>                   | A assinatura não tem atributos de [*Authenticode*](../secgloss/a-gly.md) .<br/> |



 

</dd> <dt>

**pAttrAuthcode**
</dt> <dd>

Especifica atributos para uma assinatura [*Authenticode*](../secgloss/a-gly.md) . Esse membro será necessário se o valor do membro **dwAttrChoice** for **signatário \_ fatores \_ attr**.

</dd> <dt>

**psAuthenticated**
</dt> <dd>

Atributos fornecidos pelo usuário autenticados adicionados à assinatura digital.

</dd> <dt>

**psUnauthenticated**
</dt> <dd>

Atributos fornecidos pelo usuário não autenticados adicionados à assinatura digital.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
