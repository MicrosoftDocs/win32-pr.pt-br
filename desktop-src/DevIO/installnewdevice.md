---
description: Instala um novo dispositivo. O usuário é solicitado a selecionar o dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Função InstallNewDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405302"
---
# <a name="installnewdevice-function"></a>Função InstallNewDevice

Instala um novo dispositivo. O usuário é solicitado a selecionar o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ Em\]
</dt> <dd>

Um alça para a janela de nível superior a ser usado para qualquer interface do usuário necessária.

</dd> <dt>

*ClassGuid* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID de classe.** Esse parâmetro é opcional. Se esse parâmetro for **NULL,** o usuário começará na página de opção de detecção. Se esse parâmetro for **GUID \_ NULL ou** GUID **\_ DEVCLASS \_ UNKNOWN,** o usuário será iniciado na página de seleção de classe.

</dd> <dt>

*pReboot* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o status de reinicialização. Esse parâmetro pode ser **DI \_ NEEDRESTART** ou **DI \_ NEEDREBOOT.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação associada. Você deve usar as [**funções LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a NewDev.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciamento de Dispositivos funções](device-management-functions.md)
</dt> </dl>

 

