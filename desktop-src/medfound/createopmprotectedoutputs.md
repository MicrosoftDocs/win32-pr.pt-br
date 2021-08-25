---
description: Cria objetos de saída protegidos para um dispositivo de vídeo.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Função CreateOPMProtectedOutputs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: fe2bcc0d190cf94a48b10f3d588ab4acd2d93913552f8ccef9d7eb92fefa598b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829056"
---
# <a name="createopmprotectedoutputs-function"></a>Função CreateOPMProtectedOutputs

> [!IMPORTANT]
> Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Cria objetos de saída protegidos para um dispositivo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pstrDeviceName* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*vos* \[ no\]
</dt> <dd>

Um membro da enumeração **\_ semântica de \_ \_ saída \_ de vídeo DXGKMDT OPM** , especificando se a saída protegida terá semântica de Copp (protocolo de proteção de saída) ou semântica OPM.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ no\]
</dt> <dd>

O número de elementos na matriz *pohOPMProtectedOutputArray* .

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ fora\]
</dt> <dd>

Recebe o número de itens que a função copia para a matriz *pohOPMProtectedOutputArray* .

</dd> <dt>

*pohOPMProtectedOutputArray* \[ fora\]
</dt> <dd>

Uma matriz que recebe identificadores para os objetos de saída protegidos. Cada identificador deve ser liberado chamando [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções OPM](opm-functions.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 
