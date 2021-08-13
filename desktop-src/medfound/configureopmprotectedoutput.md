---
description: Configura um objeto de saída protegido.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: Função ConfigureOPMProtectedOutput
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f62d310526d95cf4ab6d1727a3ba43eec147f320b04c0692a89d52305b7f3589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743543"
---
# <a name="configureopmprotectedoutput-function"></a>Função ConfigureOPMProtectedOutput

> [!IMPORTANT]
> Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Configura um objeto de saída protegido.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opoOPMProtectedOutput* \[ no\]
</dt> <dd>

Um identificador para o objeto de saída protegido. Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura **DXGKMDT \_ OPM \_ configure \_ Parameters** que contém o comando de configuração.

</dd> <dt>

*ulAdditionalParametersSize* \[ no\]
</dt> <dd>

O tamanho do buffer *pbAdditionalParameters* , em bytes.

</dd> <dt>

*pbAdditionalParameters* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém informações adicionais para o comando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) em vez de chamar essa função.

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

 

 
