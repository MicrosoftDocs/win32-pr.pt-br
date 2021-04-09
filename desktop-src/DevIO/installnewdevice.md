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
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089441"
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

*hwndParent* \[ no\]
</dt> <dd>

Um identificador para a janela de nível superior a ser usado para qualquer interface do usuário necessária.

</dd> <dt>

*ClassGuid* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** de classe. Esse parâmetro é opcional. Se esse parâmetro for **nulo**, o usuário será iniciado na página opção de detecção. Se esse parâmetro for **GUID \_ NULL** ou **GUID \_ DEVCLASS \_ Unknown**, o usuário será iniciado na página de seleção de classe.

</dd> <dt>

*Preboot* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o status de reinicialização. Esse parâmetro pode ser **di \_ NEEDRESTART** ou **di \_ NEEDREBOOT**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a NewDev.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de gerenciamento de dispositivo](device-management-functions.md)
</dt> </dl>

 

