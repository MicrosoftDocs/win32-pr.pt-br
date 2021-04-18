---
title: Enumeração de BITS_FILE_PROPERTY_ID (Deliveryoptimization. h)
description: A enumeração BITS_FILE_PROPERTY_ID especifica valores que definem valores de ID correspondentes às propriedades BackgroundCopyFile.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- Enumeração de BITS_FILE_PROPERTY_ID
- Enumeração de BITS_FILE_PROPERTY_ID
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
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766513"
---
# <a name="bits_file_property_id-enumeration"></a>Enumeração de BITS_FILE_PROPERTY_ID

A enumeração **BITS_FILE_PROPERTY_ID** especifica valores que definem valores de ID correspondentes às propriedades **BackgroundCopyFile** .

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





