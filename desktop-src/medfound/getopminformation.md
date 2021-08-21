---
description: Envia uma solicitação de status do OPM para um objeto de saída protegido.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: Função GetOPMInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777296"
---
# <a name="getopminformation-function"></a>Função GetOPMInformation

> [!IMPORTANT]
> Essa função é usada pelo [OPM (Gerenciador](output-protection-manager.md) de Proteção de Saída) para acessar a funcionalidade no driver de exibição. Os aplicativos não devem chamar essa função.

 

Envia uma solicitação de status do OPM para um objeto de saída protegido.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opoOPMProtectedOutput* \[ Em\]
</dt> <dd>

Um identificador para o objeto de saída protegido. Esse handle é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ Em\]
</dt> <dd>

Um ponteiro para uma **estrutura GET \_ INFO \_ \_ \_ PARAMETERS do OPM DXGKMDT** que contém dados de entrada para a solicitação de status.

</dd> <dt>

*pRequestedInformation* \[ out\]
</dt> <dd>

Um ponteiro para uma **estrutura DXGKMDT \_ OPM \_ REQUESTED \_ INFORMATION** que recebe os resultados da solicitação de status.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará STATUS \_ SUCCESS.** Caso contrário, retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Os aplicativos [**devem chamar IOPMVideoOutput::GetInformation em**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) vez de chamar essa função.

O objeto de saída protegido deve ser criado com semântica do OPM. Consulte [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

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

 

 
