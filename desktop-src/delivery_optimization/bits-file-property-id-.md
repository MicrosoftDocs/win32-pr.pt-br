---
title: BITS_FILE_PROPERTY_ID enumeração (Deliveryoptimization.h)
description: A BITS_FILE_PROPERTY_ID especifica valores que definem valores de ID correspondentes às propriedades BackgroundCopyFile.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- BITS_FILE_PROPERTY_ID enumeração
- BITS_FILE_PROPERTY_ID enumeração
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eb8593e018a5c38c6788dfffefe827ed2e086774aedca1d051680b9cb6a433a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810770"
---
# <a name="bits_file_property_id-enumeration"></a>BITS_FILE_PROPERTY_ID enumeração

A **BITS_FILE_PROPERTY_ID** especifica valores que definem valores de ID correspondentes às **propriedades BackgroundCopyFile.**

## <a name="syntax"></a>Syntax


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**
</dt> <dd>

O conjunto completo de cabeçalhos de resposta HTTP do último pacote de resposta HTTP do servidor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



 

 





