---
description: A função InstallWiaDevice instala um Windows WIA (Aquisição de Imagem) como dispositivo enumerado como raiz. Ele poderá abrir um aviso de segurança se qualquer arquivo ou coinstalador de instalação não for assinado digitalmente e confiável.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Função InstallWiaDevice (Wia.h)
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
ms.openlocfilehash: 10006e234c9a76054a77fb64f89a31d9a21e394066bcc98813912bad9f804e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965835"
---
# <a name="installwiadevice-function"></a>Função InstallWiaDevice

A **função InstallWiaDevice** instala um Windows WIA (Aquisição de Imagem) como dispositivo enumerado como raiz. Ele poderá abrir um aviso de segurança se qualquer arquivo ou coinstalador de instalação não for assinado digitalmente e confiável.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaDeviceInstall* \[ Em\]
</dt> <dd>

Tipo: **PWIADEVICEINSTALL \***

Ponteiro para uma estrutura WIADEVICEINSTALL. O *membro szFriendlyName* da estrutura deve ser definido como o dispositivo FriendlyName real.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **DWORD**

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, ela retornará um código de erro Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




