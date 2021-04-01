---
description: Especifica atributos para uma assinatura Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Estrutura de SIGNER_ATTR_AUTHCODE
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
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922879"
---
# <a name="signer_attr_authcode-structure"></a>\_Estrutura de fatores attr de signatário \_

A **estrutura \_ \_ fatores attr de signatário** especifica atributos para uma assinatura [*Authenticode*](../secgloss/a-gly.md) .

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

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

**True** para assinar o assunto como um editor comercial; caso contrário, **false**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**True** para assinar o assunto como um Publicador individual; caso contrário, **false**.

</dd> <dt>

**pwszName**
</dt> <dd>

O nome de exibição do arquivo no download.

</dd> <dt>

**pwszInfo**
</dt> <dd>

O nome de exibição da URL do arquivo durante o download.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de assinatura do assinante \_**](signer-signature-info.md)
</dt> </dl>

 

 
