---
description: Recupera um identificador de objeto para o objeto especificado associado ao processo especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Função ObFindHandleForObject (Ntosp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 481def34e3e8656205eefe96058fe3c7558d2c898c7e05ddc78f9a67435c507e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984146"
---
# <a name="obfindhandleforobject-function"></a>Função ObFindHandleForObject

\[Essa função é obsoleta e pode ser alterada ou não disponível em versões futuras do Windows. Evite usar essa função.\]

Recupera um identificador de objeto para o objeto especificado associado ao processo especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Processo* \[ Em\]
</dt> <dd>

O processo. Esse handle é retornado pela **função IoGetCurrentProcess** ou **PsGetCurrentProcess.**

</dd> <dt>

*Objeto* \[ Em\]
</dt> <dd>

Um ponteiro para o objeto .

</dd> <dt>

*Reservado1* \[ in, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Reservado2* \[ in, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Manipular* \[ out\]
</dt> <dd>

O identificador de objeto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retornará **TRUE** se uma corresponder for encontrada e **FALSE caso contrário.**

## <a name="remarks"></a>Comentários

Essa função está disponível no Ntoskrnl.exe e pode ser chamada somente no modo kernel. A biblioteca de importação correspondente está disponível por meio do WDK (Kit Windows Driver).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ntosp.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Ntoskrnl.lib</dt> </dl> |



 

 




