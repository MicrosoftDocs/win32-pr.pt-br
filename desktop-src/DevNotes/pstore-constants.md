---
description: As constantes a seguir são usadas por Pstore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Constantes Pstore (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755919"
---
# <a name="pstore-constants"></a>Constantes de Pstore

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

As constantes a seguir são usadas por Pstore.

Códigos de erro de armazenamento protegido



| Constante/valor                                                                                                                                                                                                                               | Descrição                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**PST \_ E \_ OK**</dt> <dt>0x00000000l</dt> </dl>                             | A operação foi bem-sucedida.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**PST \_ O \_ tipo E \_ existe**</dt> <dt>0x800C0004L</dt> </dl> | O item de dados já existe no armazenamento protegido. <br/> |



Valores de cláusula de acesso



| Constante/valor                                                                                                                                                                                                                                      | Descrição                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**PST \_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Aponta para uma estrutura de [**\_ AUTHENTICODEDATA de PST**](pst-authenticodedata.md) .<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **\_ \_ Seleção binária de PST**</dt> <dt>2</dt> </dl>                   | Aponta para uma estrutura de **\_ BINARYCHECKDATA de PST** .<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**PST \_ \_Descritor de segurança**</dt> <dt>4</dt> </dl> | Aponta para um descritor de segurança válido do Windows. <br/>                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
