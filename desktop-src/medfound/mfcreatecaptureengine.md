---
description: Cria uma instância do mecanismo de captura.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Função MFCreateCaptureEngine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766520"
---
# <a name="mfcreatecaptureengine-function"></a>Função MFCreateCaptureEngine

\[MFCreateCaptureEngine não tem suporte e pode ser alterado ou indisponível no futuro. \]

Cria uma instância do mecanismo de captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCaptureEngine* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) . O chamador deve liberar a interface.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, ela retornará S \_ OK. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada e não está declarada em um arquivo de cabeçalho público. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a MFCaptureEngine.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
