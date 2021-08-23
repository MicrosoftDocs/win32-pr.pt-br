---
description: Especifica atributos para uma assinatura Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cce522403e4b4e416bd3d1ecb9d6c4a551ef3bb67407f853f586bd061f3d8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898943"
---
# <a name="signer_attr_authcode-structure"></a>Estrutura \_ SIGNER ATTR \_ AUTHCODE

A **estrutura \_ SIGNER ATTR \_ AUTHCODE** especifica atributos para uma [*assinatura Authenticode.*](../secgloss/a-gly.md)

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de header. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**fCommercial**
</dt> <dd>

**TRUE** para assinar o assunto como um editor comercial; caso contrário, **FALSE.**

</dd> <dt>

**fIndividual**
</dt> <dd>

**TRUE** para assinar o assunto como um publicador individual; caso contrário, **FALSE.**

</dd> <dt>

**pwszName**
</dt> <dd>

O nome de exibição do arquivo após o download.

</dd> <dt>

**pwszInfo**
</dt> <dd>

O nome de exibição da URL do arquivo após o download.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DE \_ ASSINATURA DO \_ SIGNER**](signer-signature-info.md)
</dt> </dl>

 

 
