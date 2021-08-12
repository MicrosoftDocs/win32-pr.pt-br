---
title: Estrutura de BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: A BITS_FILE_PROPERTY_VALUE Union fornece o valor da Propriedade do arquivo do com base em um valor da enumeração BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Estrutura de BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba01a8c83cef842c40149b3fe8cbc586a7da5f819ffc387befb9f84182cbce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544621"
---
# <a name="bits_file_property_value-structure"></a>Estrutura de BITS_FILE_PROPERTY_VALUE

A **BITS_FILE_PROPERTY_VALUE** Union fornece o valor da Propriedade do arquivo do com base em um valor da enumeração [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Cadeia de caracteres**
</dt> <dd>

Esse valor é usado ao usar o valor de enumeração da ID de propriedade **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





