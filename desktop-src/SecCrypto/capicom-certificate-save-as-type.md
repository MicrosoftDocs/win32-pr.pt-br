---
description: Define o formato de um arquivo que contém informações de certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772637"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>Enumeração CAPICOM \_ CERTIFICATE \_ SAVE AS \_ \_ TYPE

O **tipo de enumeração CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE** define o formato de um arquivo que contém informações de certificado. Esse tipo de enumeração foi introduzido pelo CAPICOM 2.0.

## <a name="members"></a>Membros



| Membro                                  | DESCRIÇÃO                                                                                                                                   | Valor |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **SALVAR CERTIFICADO CAPICOM \_ \_ COMO \_ \_ PFX** | O arquivo de saída será formatado como um arquivo PFX (PKCS 12) e todas as chaves privadas associadas que são exportáveis também serão salvas.<br/> | 0     |
| **CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ CER** | O arquivo de saída será formatado como um arquivo CER sem chaves privadas salvas.<br/>                                                        | 1     |



## <a name="remarks"></a>Comentários

O **tipo de enumeração CAPICOM \_ CERTIFICATE SAVE AS \_ \_ \_ TYPE** é usado pelo [**método Certificate.Save.**](certificate-save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




