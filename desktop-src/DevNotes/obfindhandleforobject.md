---
description: Recupera um identificador de objeto para o objeto especificado associado ao processo especificado.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Função ObFindHandleForObject (Ntosp. h)
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
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826224"
---
# <a name="obfindhandleforobject-function"></a>Função ObFindHandleForObject

\[Essa função é obsoleta e pode ser alterada ou indisponível em versões futuras do Windows. Evite usar essa função.\]

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

*Processo* \[ do no\]
</dt> <dd>

O processo. Esse identificador é retornado pela função **IoGetCurrentProcess** ou **PsGetCurrentProcess** .

</dd> <dt>

*Objeto* \[ do no\]
</dt> <dd>

Um ponteiro para o objeto.

</dd> <dt>

*Reserved1* \[ em, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Reserved2* \[ em, opcional\]
</dt> <dd>

Reservado.

</dd> <dt>

*Identificador* \[ do fora\]
</dt> <dd>

O identificador de objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retornará **true** se uma correspondência for encontrada e **false** caso contrário.

## <a name="remarks"></a>Comentários

Essa função está disponível em Ntoskrnl.exe e pode ser chamada somente do modo kernel. A biblioteca de importação correspondente está disponível por meio do WDK (Windows Driver Kit).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Ntosp. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Ntoskrnl. lib</dt> </dl> |



 

 




