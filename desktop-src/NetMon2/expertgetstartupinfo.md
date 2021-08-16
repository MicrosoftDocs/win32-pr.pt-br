---
description: A função ExpertGetStartupInfo recupera as informações de configuração de inicialização para o especialista.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Função ExpertGetStartupInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7e4327965dce1c4bca07846a818609e555c16a3a27b0a19204a9971eaf9d642e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366878"
---
# <a name="expertgetstartupinfo-function"></a>Função ExpertGetStartupInfo

A função **ExpertGetStartupInfo** recupera as informações de configuração de inicialização para o especialista.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hExpertKey* \[ no\]
</dt> <dd>

Identificador de especialista exclusivo. Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .

</dd> <dt>

*pExpertStartupInfo* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) que contém informações de inicialização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será NMERR.

## <a name="remarks"></a>Comentários

A função **ExpertGetStartupInfo** será usada se o especialista precisar determinar as informações de inicialização usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




