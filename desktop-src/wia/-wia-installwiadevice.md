---
description: A função InstallWiaDevice instala um dispositivo de aquisição de imagem do Windows (WIA) como dispositivo enumerado por raiz. Ele poderá avisar um aviso de segurança se qualquer arquivo de instalação ou o instalador não for assinado digitalmente e confiável.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Função InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647490"
---
# <a name="installwiadevice-function"></a>Função InstallWiaDevice

A função **InstallWiaDevice** instala um dispositivo de aquisição de imagem do Windows (WIA) como dispositivo enumerado por raiz. Ele poderá avisar um aviso de segurança se qualquer arquivo de instalação ou o instalador não for assinado digitalmente e confiável.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaDeviceInstall* \[ no\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \** _

Ponteiro para uma estrutura WIADEVICEINSTALL. O membro _szFriendlyName * da estrutura deve ser definido como o dispositivo FriendlyName real.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **DWORD**

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, ela retornará um código de erro Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




