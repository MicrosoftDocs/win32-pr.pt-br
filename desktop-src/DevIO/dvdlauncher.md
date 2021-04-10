---
description: Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: Função DvdLauncher
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089442"
---
# <a name="dvdlauncher-function"></a>Função DvdLauncher

Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela de nível superior a ser usado para qualquer interface do usuário necessária.

</dd> <dt>

*Letra_da_unidade* \[ no\]
</dt> <dd>

A letra da unidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido e as regiões corresponderem, o valor de retorno será diferente de zero. Caso contrário, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a StorProp.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de gerenciamento de dispositivo](device-management-functions.md)
</dt> </dl>

 

