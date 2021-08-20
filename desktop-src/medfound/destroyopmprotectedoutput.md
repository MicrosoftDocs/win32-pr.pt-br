---
description: Libera um objeto de saída protegido.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: Função DestroyOPMProtectedOutput
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 5a30f4f4666b2da2e9b1fc38c90f51da9264f4656f82ac11f7abd55b498419e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742365"
---
# <a name="destroyopmprotectedoutput-function"></a>Função DestroyOPMProtectedOutput

> [!IMPORTANT]
> Essa função é usada pelo [OPM (Gerenciador](output-protection-manager.md) de Proteção de Saída) para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Libera um objeto de saída protegido.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opoOPMProtectedOutput* \[ Em\]
</dt> <dd>

Um identificador para o objeto de saída protegido. Esse handle é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

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

 

 
