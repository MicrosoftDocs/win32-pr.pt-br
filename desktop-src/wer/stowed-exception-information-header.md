---
title: STOWED_EXCEPTION_INFORMATION_HEADER estrutura
description: Contém informações que identificam a estrutura pai.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER estrutura Relatório de Erros do Windows
- PSTOWED_EXCEPTION_INFORMATION_HEADER ponteiro de estrutura Relatório de Erros do Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bc77cadd9e69dda64470434ffbc29947c219d5d358d2e3c47be122663cfe35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670722"
---
# <a name="stowed_exception_information_header-structure"></a>Estrutura DE HEADER \_ DE \_ INFORMAÇÕES DE EXCEÇÃO \_ DE STOWED

Contém informações que identificam a estrutura pai.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho, em bytes, da estrutura pai.

</dd> <dt>

**Assinatura**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um valor de 32 bits que especifica a assinatura da estrutura pai.



| Valor                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**STOWED \_ INFORMAÇÕES \_ DE \_ EXCEÇÃO \_ V1 ASSINATURA**</dt> <dt>'SE01'</dt> </dl> | Esse valor indica que o pai é uma estrutura **STOWED \_ EXCEPTION \_ INFORMATION \_ V1.**<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**STOWED \_ INFORMAÇÕES \_ DE \_ EXCEÇÃO \_ ASSINATURA V2**</dt> <dt>'SE02'</dt> </dl> | Esse valor indica que o pai é uma estrutura [**STOWED \_ EXCEPTION \_ INFORMATION \_ V2.**](stowed-exception-information-v2.md)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

[**STOWED \_ AS \_ INFORMAÇÕES \_ DE EXCEÇÃO V2**](stowed-exception-information-v2.md) e O HEADER DE INFORMAÇÕES DE EXCEÇÃO STOWED atualmente não estão definidos em um **\_ \_ \_ header** que está disponível publicamente, portanto, você precisa defini-las em seu código-fonte antes de usá-las.

A **estrutura STOWED \_ EXCEPTION INFORMATION \_ \_ V1** é idêntica a essa estrutura, exceto que ela não contém os membros **NestedExceptionType** e **NestedException.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Nenhum</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DE \_ EXCEÇÃO \_ FORNECIDAS \_ V2**](stowed-exception-information-v2.md)
</dt> </dl>

 

