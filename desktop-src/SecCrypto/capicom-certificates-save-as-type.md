---
description: Define o formato de um arquivo que contém informações de certificados.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumeração de CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879365"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>\_Enumeração de certificados de CApicom \_ \_ de gravação como \_ tipo

O tipo de enumeração **\_ \_ Salvar \_ \_ como certificado de CAPICOM certificados** define o formato de um arquivo que contém informações de certificados. Esse tipo de enumeração foi introduzido pelo CAPICOM 2,0.

## <a name="members"></a>Membros



| Membro                                          | DESCRIÇÃO                                          | Valor |
|-------------------------------------------------|------------------------------------------------------|-------|
| **os certificados CAPICOM \_ \_ Salvar \_ como \_ serializado** | Os certificados salvos são serializados.<br/>    | 0     |
| **Os certificados CAPICOM \_ \_ Save \_ as \_ PKCS7**      | Os certificados são salvos como um PKCS \# 7.<br/> | 1     |
| **os certificados CAPICOM \_ \_ Salvar \_ como \_ pfx**        | Os certificados são salvos como um PFX.<br/>      | 2     |



## <a name="remarks"></a>Comentários

O \_ tipo de enumeração ' salvar como tipo ' certificados CApicor \_ \_ \_ é usado pelo método [**Certificates. Save**](certificates-save.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




