---
description: Obtém o tamanho da matriz que deve ser alocada antes de chamar CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Função GetSuggestedOPMProtectedOutputArraySize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: c84738fe37661d2a593432b571c6022b0369e28ee3b2a3cb028b8eb84276a21a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879373"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a>Função GetSuggestedOPMProtectedOutputArraySize

> [!IMPORTANT]
> Essa função é usada pelo [OPM (Gerenciador](output-protection-manager.md) de Proteção de Saída) para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Obtém o tamanho da matriz que deve ser alocada antes de chamar [**CreateOPMProtectedOutputs.**](createopmprotectedoutputs.md)

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pstrDeviceName* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ STRING UNICODE**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de exibição, conforme retornado pela [**função GetMonitorInfo.**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa)

</dd> <dt>

*pdwSuggestedOPMProtectedOutputArraySize* \[ out\]
</dt> <dd>

Recebe o tamanho que deve ser alocado para a matriz, em número de elementos de matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará STATUS \_ SUCCESS.** Caso contrário, retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação associada. Para chamar essa função, você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções OPM](opm-functions.md)
</dt> <dt>

[Gerenciador de Proteção de Saída](output-protection-manager.md)
</dt> </dl>

 

 
