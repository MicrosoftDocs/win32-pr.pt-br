---
description: Define o formato de um arquivo que contém informações de certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumeração de CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
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
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754608"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ Enumeração de tipo de \_ certificado capicor

O tipo de enumeração do **certificado CAPICOM \_ \_ Salvar \_ como \_ tipo** define o formato de um arquivo que contém informações de certificado. Esse tipo de enumeração foi introduzido pelo CAPICOM 2,0.

## <a name="members"></a>Membros



| Membro                                  | DESCRIÇÃO                                                                                                                                   | Valor |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_salvar certificado de CApicom \_ \_ como \_ pfx** | O arquivo de saída será formatado como um arquivo PFX (PKCS 12) e quaisquer chaves privadas associadas que sejam exportáveis também serão salvas.<br/> | 0     |
| **\_salvar certificado de CApicom \_ \_ como \_ cer** | O arquivo de saída será formatado como um arquivo CER sem chaves privadas salvas.<br/>                                                        | 1     |



## <a name="remarks"></a>Comentários

O tipo de enumeração do **certificado de CAPICOM \_ \_ Salvar \_ como \_ tipo** é usado pelo método [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




