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
ms.openlocfilehash: 18d264b30b8f3ed4d06e80f236908dd7bc81dbe96c4eb9c3231fa330331e34f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940246"
---
# <a name="mfcreatecaptureengine-function"></a>Função MFCreateCaptureEngine

\[Não há suporte para MFCreateCaptureEngine e pode ser alterado ou não disponível no futuro. \]

Cria uma instância do mecanismo de captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCaptureEngine* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IMFCaptureEngine.**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) O chamador deve liberar a interface.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará S \_ OK. Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação associada e não é declarada em um arquivo de header público. Você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a MFCaptureEngine.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation funções](media-foundation-functions.md)
</dt> </dl>

 

 
