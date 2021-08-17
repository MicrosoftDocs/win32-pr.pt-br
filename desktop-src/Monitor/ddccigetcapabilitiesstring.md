---
title: Função DDCCIGetCapabilitiesString
description: Obtém uma cadeia de caracteres que descreve os recursos de um monitor.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configuração do monitor de função DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f21cf89ef459e2585dda9f05e4f16d032949d423c627225380481d71c59400d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806124"
---
# <a name="ddccigetcapabilitiesstring-function"></a>Função DDCCIGetCapabilitiesString

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Obtém uma cadeia de caracteres que descreve os recursos de um monitor.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HMONITOR* \[ no\]
</dt> <dd>

Um identificador para um monitor físico.

</dd> <dt>

*pszString* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe a cadeia de caracteres de recursos. Para obter o comprimento da cadeia de caracteres de recursos, chame [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).

</dd> <dt>

*dwLength* \[ no\]
</dt> <dd>

O tamanho do buffer *pszString* , em caracteres, incluindo o caractere nulo de terminação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) em vez de chamar essa função.

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Monitorar funções de configuração](monitor-configuration-functions.md)
</dt> </dl>

 

