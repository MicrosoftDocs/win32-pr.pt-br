---
title: Estrutura de STOWED_EXCEPTION_INFORMATION_HEADER
description: Contém informações que identificam a estrutura pai.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Estrutura de STOWED_EXCEPTION_INFORMATION_HEADER Relatório de Erros do Windows
- Ponteiro de estrutura de PSTOWED_EXCEPTION_INFORMATION_HEADER Relatório de Erros do Windows
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
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009676"
---
# <a name="stowed_exception_information_header-structure"></a>Estrutura de \_ \_ cabeçalho de informações de exceção dedevida \_

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

**Signature**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Um valor de 32 bits que especifica a assinatura da estrutura pai.



| Valor                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> Em <dt>**DEdevido \_ \_Informações de \_ exceção \_ assinatura v1**</dt> <dt>' SE01 '</dt> </dl> | Esse valor indica que o pai é uma estrutura de informações de exceção de nível **\_ \_ \_ v1** .<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> Em <dt>**DEdevido \_ \_ \_ \_ Assinatura de informações de exceção v2**</dt> <dt>' SE02 '</dt> </dl> | Esse valor indica que o pai é uma estrutura de [**\_ \_ informações de \_ exceção dedevida**](stowed-exception-information-v2.md) .<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Em [**DEdevido \_ \_As informações \_ de exceção v2**](stowed-exception-information-v2.md) e o **cabeçalho de \_ \_ informações \_ de exceção dedevida** não são definidas atualmente em um cabeçalho disponível publicamente, portanto, você precisa defini-las no código-fonte antes de usá-las.

A estrutura de informações de exceção devidada **\_ \_ \_ v1** é idêntica a essa estrutura, exceto que ela não contém os membros **NestedExceptionType** e **aninhaexception** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Nenhuma</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Informações de exceção dedevidas \_ \_ \_ v2**](stowed-exception-information-v2.md)
</dt> </dl>

 

