---
description: Contém informações estendidas do módulo.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Estrutura de AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748098"
---
# <a name="aux_module_extended_info-structure"></a>\_Estrutura de \_ informações estendidas do módulo aux \_

Contém informações estendidas do módulo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**BasicInfo**
</dt> <dd>

Uma estrutura de [**\_ \_ \_ informações básicas do módulo aux**](aux-module-basic-info-struct.md) .

</dd> <dt>

**ImageSize**
</dt> <dd>

O tamanho, em bytes, do módulo carregado.

</dd> <dt>

**FileNameOffset**
</dt> <dd>

O deslocamento do nome do arquivo dentro do buffer de **fullpathname** .

</dd> <dt>

**FullPathname**
</dt> <dd>

O caminho completo do módulo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de API auxiliar do Windows versão 1,0 ou posterior<br/>                          |
| parâmetro<br/>          | <dl> <dt>\_Klib aux. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**\_ \_ informações básicas do módulo aux \_**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




